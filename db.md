erDiagram
      
"dbo.ActivityMessageContent" {
    int Activity_id "PK, FK"
          nvarchar(-1) Content ""
          bit IsDeleted ""
          datetime Deleted ""
          nvarchar(-1) RichContent ""
          
}
"dbo.HeroBlockTemplate" {
    int Id "PK"
          nvarchar(255) Type ""
          int Position ""
          
}
"dbo.UserSkills" {
    int Id "PK"
          bit Approved ""
          datetime ApprovedDate ""
          datetime Created ""
          int User_id "FK"
          int Skill_id "FK"
          
}
"dbo.ActivityMetadataProperty" {
    int Id "PK"
          nvarchar(255) Name ""
          nvarchar(-1) Value ""
          int Activity_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.HeroBlockTranslation" {
    int HeroBlock_id "PK, FK"
          int Lcid "PK"
          nvarchar(255) Title ""
          nvarchar(255) SubTitle ""
          nvarchar(2000) Description ""
          nvarchar(2000) SourceUrl ""
          nvarchar(2000) ImageUrl ""
          nvarchar(2000) VideoUrl ""
          nvarchar(2000) LinkUrl ""
          bit LinkInNewWindow ""
          nvarchar(-1) CodeSchema ""
          nvarchar(2000) SourceDataUrl ""
          
}
"dbo.UserToNotification" {
    int Notification_id "PK, FK"
          int User_id "PK, FK"
          datetime Created ""
          
}
"dbo.ActivityReports" {
    int Id "PK"
          datetime Created ""
          nvarchar(255) Type ""
          nvarchar(-1) Comments ""
          nvarchar(255) Status ""
          int Activity_id "FK"
          int Comment_id "FK"
          int User_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.HeroTemplate" {
    int Id "PK"
          nvarchar(255) Name ""
          bit IsEnabled ""
          
}
"dbo.ZoneInstance" {
    int Id "PK"
          datetime Created ""
          int PageTemplate_id "FK"
          int LayoutZone_id "FK"
          int GroupPage_id "FK"
          int GroupPageTranslation_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.ActivityTerm" {
    int Activity_id "PK, FK"
          int Term_id "PK, FK"
          
}
"dbo.HeroTemplateBlockTemplate" {
    int HeroTemplate_id "PK, FK"
          int HeroBlockTemplate_id "PK, FK"
          
}
"dbo.ActivityTranslation" {
    int Id "PK"
          nvarchar(-1) Message ""
          nvarchar(255) Title ""
          int LCID ""
          bit IsPublished ""
          datetime PublishedDate ""
          nvarchar(255) Description ""
          nvarchar(2048) Url ""
          nvarchar(255) ListGuid ""
          int ItemId ""
          int Activity_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          nvarchar(-1) RichContent ""
          
}
"dbo.HeroWidgetBlockContent" {
    int HeroWidgetBlock_id "PK, FK"
          nvarchar(-1) CodeSchema ""
          nvarchar(-1) CodeContent ""
          nvarchar(-1) CodeStyling ""
          nvarchar(2000) SourceDataUrl ""
          int CodeType ""
          int UrlSourceType ""
          uniqueidentifier PowerAutomateId ""
          
}
"dbo.WebhookSubscription" {
    int Id "PK"
          nvarchar(255) SubscriptionId ""
          nvarchar(255) ListId ""
          datetime CreationDate ""
          datetime ExpirationDate ""
          nvarchar(255) LastChangesToken ""
          nvarchar(255) PlaceUrl ""
          nvarchar(255) NotificationUrl ""
          
}
"dbo.ActivityUserSection" {
    int Activity_id "FK"
          int UserSection_id "FK"
          
}
"dbo.Language" {
    int LCID "PK"
          nvarchar(255) Code ""
          nvarchar(255) Name ""
          bit IsActive ""
          
}
"dbo.ActivityViews" {
    int Id "PK"
          int Views ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.Layout" {
    int Id "PK"
          nvarchar(255) Title ""
          datetime Created ""
          
}
"ContentStorage.EditorialBlogPostVersion" {
    int ContentId "PK"
          nvarchar(-1) Title ""
          nvarchar(-1) Body ""
          nvarchar(-1) BodyMetadata ""
          
}
"dbo.AllowedModules" {
    int Id "PK"
          nvarchar(255) Type ""
          datetime Created ""
          int LayoutZone_id "FK"
          
}
"dbo.LayoutZone" {
    int Id "PK"
          nvarchar(255) Title ""
          int Width ""
          datetime Created ""
          int Layout_id "FK"
          
}
"dbo.App" {
    int Id "PK"
          nvarchar(255) Title ""
          nvarchar(2000) Link ""
          nvarchar(-1) Description ""
          nvarchar(255) UIAccess ""
          bit Featured ""
          nvarchar(255) Icon ""
          nvarchar(50) BackgroundColor ""
          datetime Created ""
          datetime Modified ""
          int LocalEntity_id "FK"
          
}
"Audit.EventLog" {
    int EventId "PK"
          nvarchar(255) EventName ""
          datetime EventDate ""
          int EntityId ""
          nvarchar(255) EntityType ""
          nvarchar(255) UserLoginName ""
          
}
"dbo.Link" {
    int Id "PK"
          nvarchar(255) Description ""
          nvarchar(255) Title ""
          nvarchar(255) Image ""
          nvarchar(255) Url ""
          
}
"dbo.AppCategory" {
    int Id "PK"
          nvarchar(255) Title ""
          int UIOrder ""
          int LocalEntity_id "FK"
          
}
"dbo.LocalEntity" {
    int Id "PK"
          nvarchar(255) Title ""
          bit IsDefaultLocalEntity ""
          int DefaultLcid ""
          bit StoriesModuleEnabled ""
          bit NavigationModuleEnabled ""
          bit PagesModuleEnabled ""
          bit HeroModuleEnabled ""
          bit SitesModuleEnabled ""
          bit DiscoveryCardsModuleEnabled ""
          bit AppsModuleEnabled ""
          bit AudiencesModuleEnabled ""
          nvarchar(255) Branding ""
          nvarchar(2048) LogoUrl ""
          nvarchar(2048) MobileLogoUrl ""
          bit AllowCustomDiscoveryCards ""
          
}
"dbo.AppCategoryApp" {
    int App_id "PK, FK"
          int AppCategory_id "PK, FK"
          
}
"dbo.LocalEntityDomainGroup" {
    int DomainGroup_id "FK, PK"
          int LocalEntity_id "FK"
          
}
"dbo.AppCategoryTranslation" {
    int Category_Id "PK, FK"
          int Lcid "PK"
          nvarchar(255) Title ""
          
}
"dbo.LocalEntityHeroBlock" {
    int HeroBlock_id "FK, PK"
          int LocalEntity_id "FK, PK"
          
}
"dbo.AppResponsible" {
    int App_id "PK, FK"
          int User_id "PK, FK"
          
}
"dbo.GroupAudience" {
    int Group_id "PK, FK"
          int Audience_id "PK, FK"
          
}
"dbo.LocalEntityHeroTemplate" {
    int HeroTemplate_id "FK, PK"
          int LocalEntity_id "FK, PK"
          datetime Schedule ""
          
}
"dbo.AppScreenshot" {
    nvarchar(255) Url "PK"
          int App_id "PK, FK"
          int UIOrder ""
          
}
"dbo.LocalEntityMember" {
    int User_id "FK, PK"
          int LocalEntity_id "FK"
          
}
"dbo.AppTranslation" {
    int App_Id "PK, FK"
          int Lcid "PK"
          nvarchar(255) Title ""
          nvarchar(-1) Description ""
          nvarchar(2000) Link ""
          
}
"dbo.LocalEntityMenuNode" {
    int Node_id "FK, PK"
          int LocalEntity_id "FK, PK"
          int NodeOrder ""
          
}
"dbo.AppUser" {
    int App_id "PK, FK"
          int User_id "PK, FK"
          int UIOrder ""
          
}
"dbo.Mentions" {
    int Activity_id "FK, PK"
          int User_id "FK, PK"
          
}
"dbo.AccessManagementUser" {
    int Id "PK"
          int User_id "FK"
          int Role ""
          bit Exclude ""
          
}
"dbo.Attachment" {
    int Id "PK"
          nvarchar(255) FileName ""
          nvarchar(2048) Url ""
          nvarchar(255) Type ""
          nvarchar(255) Provider ""
          nvarchar(255) Title ""
          nvarchar(-1) Description ""
          nvarchar(2048) IconUrl ""
          bigint Size ""
          nvarchar(255) Version ""
          smallint Visibility ""
          datetime Created ""
          datetime LastModified ""
          nvarchar(255) Subtype ""
          int Views ""
          bit Highlighted ""
          nvarchar(255) ListGuid ""
          int ItemId ""
          nvarchar(2048) PreviewImageUrl ""
          nvarchar(-1) PreviewHtml ""
          int Activity_id "FK"
          int Creator_id "FK"
          int LastModifiedBy_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.MenuItem" {
    int Id "PK"
          nvarchar(55) Title ""
          nvarchar(2000) LinkUrl ""
          bit LinkInNewWindow ""
          nvarchar(255) ImageUrl ""
          int ItemOrder ""
          int Section_id "FK"
          
}
"dbo.Audience" {
    int Id "PK"
          nvarchar(255) Name ""
          int Order ""
          int Category_id "FK"
          int ParentAudience_id "FK"
          int MainRule_id "FK"
          
}
"dbo.MenuItemTranslation" {
    int Id "PK"
          nvarchar(55) Title ""
          nvarchar(2000) LinkUrl ""
          nvarchar(255) ImageUrl ""
          int LCID ""
          int MenuItem_id "FK"
          
}
"dbo.AccessManagementDomainGroup" {
    int Id "PK"
          int DomainGroup_id "FK"
          int Role ""
          bit Exclude ""
          
}
"dbo.AudienceCategory" {
    int Id "PK"
          nvarchar(255) Title ""
          int Order ""
          
}
"dbo.EulaTranslation" {
    int Lcid "PK"
          nvarchar(50) Title ""
          nvarchar(-1) Content ""
          nvarchar(80) AgreementText ""
          nvarchar(25) AcceptanceText ""
          
}
"dbo.MenuNode" {
    int Id "PK"
          nvarchar(55) Title ""
          bit Enabled ""
          bit IsDefault ""
          bit Shown ""
          nvarchar(10) PlaceHolder ""
          nvarchar(2000) LinkUrl ""
          bit LinkInNewWindow ""
          nvarchar(255) ConfigurationDependency ""
          nvarchar(50) Type ""
          
}
"dbo.AudienceUser" {
    int Audience_id "PK, FK"
          int User_id "PK, FK"
          bit IsFromDomainGroup ""
          
}
"dbo.MenuNodeSection" {
    int Node_id "FK, PK"
          int Section_id "FK, PK"
          nvarchar(255) Layout ""
          int SectionOrder ""
          
}
"dbo.RbacUser" {
    int Id "PK"
          int User_id "FK"
          int Role ""
          
}
"dbo.Bookmarks" {
    int Activity_id "PK, FK"
          int User_id "PK, FK"
          
}
"dbo.MenuNodeTranslation" {
    int Id "PK"
          nvarchar(55) Title ""
          nvarchar(2000) LinkUrl ""
          int LCID ""
          int MenuNode_id "FK"
          
}
"dbo.Channel" {
    int Id "PK"
          nvarchar(250) Title ""
          nvarchar(250) Description ""
          nvarchar(255) LinkUrl ""
          nvarchar(255) ImageUrl ""
          datetime Created ""
          int Category_id "FK"
          int Group_id "FK"
          bit IsRestricted ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.MenuSection" {
    int Id "PK"
          nvarchar(255) Type ""
          nvarchar(55) Title ""
          
}
"dbo.ChannelAudience" {
    int Audience_id "FK"
          int Channel_id "FK"
          
}
"dbo.ChannelCategory" {
    int Id "PK"
          nvarchar(255) Title ""
          datetime Created ""
          int Group_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.LocalEntityAdmin" {
    int User_id "PK, FK"
          int LocalEntity_id "PK, FK"
          
}
"dbo.MenuSectionMetadataProperty" {
    int Id "PK"
          nvarchar(55) Name ""
          nvarchar(-1) Value ""
          int Section_id "FK"
          
}
"dbo.ChannelFollow" {
    int User_id "PK, FK"
          int Channel_id "PK, FK"
          bit IsFromAudience ""
          bit IsFromUser ""
          
}
"dbo.MenuSectionTranslation" {
    int Id "PK"
          nvarchar(55) Title ""
          int LCID ""
          int MenuSection_id "FK"
          
}
"dbo.ChannelOwner" {
    int Channel_id "PK, FK"
          int User_id "PK, FK"
          
}
"dbo.ModuleInstance" {
    int Id "PK"
          datetime Created ""
          bit Hidden ""
          nvarchar(-1) Settings ""
          nvarchar(255) Type ""
          int Position ""
          int ZoneInstance_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.Comment" {
    int Id "PK"
          nvarchar(-1) Message ""
          datetime Created ""
          datetime LastModified ""
          nvarchar(255) Device ""
          smallint Visibility ""
          int Activity_id "FK"
          int User_id "FK"
          int LastEditor_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.MyItemsCategory" {
    int Id "PK"
          nvarchar(255) Name ""
          int User_id "FK"
          int Group_id "FK"
          
}
"dbo.CommentLikes" {
    int Comment_id "PK, FK"
          int User_id "PK, FK"
          datetime Created ""
          
}
"dbo.MyItemsCategoryCommunicationPage" {
    int Category "FK, PK"
          int CommunicationPage "FK, PK"
          int PreviousCategory "FK"
          int PreviousCommunicationPage "FK"
          int NextCategory "FK"
          int NextCommunicationPage "FK"
          
}
"dbo.CommunicationPageAction" {
    int Id "PK"
          nvarchar(255) Type ""
          datetime Created ""
          datetime LastModified ""
          nvarchar(500) Message ""
          int CommunicationPageDetail_id "FK"
          int User_id "FK"
          nvarchar(255) Status ""
          int RequestId "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.CommunicationPageAuthor" {
    int User_id "PK, FK"
          int CommunicationPage_id "PK, FK"
          bit IsPublic ""
          
}
"dbo.CommunicationPageChannel" {
    int Channel_id "PK, FK"
          int CommunicationPageDetail_id "PK, FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.Notification" {
    int Id "PK"
          nvarchar(255) Reason ""
          nvarchar(255) Message ""
          datetime Created ""
          bit IsRead ""
          bit IsProcessed ""
          datetime ReadDate ""
          bit HasBeenPushed ""
          datetime PushDate ""
          int Activity_id "FK"
          int Group_id "FK"
          int Destinatary_id "FK"
          int App_id "FK"
          nvarchar(-1) MetaData ""
          
}
"dbo.CommunicationPageDetail" {
    int ActivityId "PK, FK"
          bit AllowComments ""
          bit AllowLikes ""
          bit Featured ""
          bit IsPublished ""
          datetime PublishedDate ""
          datetime Schedule ""
          nvarchar(255) BackgroundImageUrl ""
          int BackgroundImageOffsetX ""
          int BackgroundImageOffsetY ""
          int BackgroundImageWidth ""
          int BackgroundImageHeight ""
          nvarchar(1024) VideoUrl ""
          nvarchar(250) BackgroundImageAlternateText ""
          datetime ExpirationDate ""
          bit IsDeleted ""
          datetime Deleted ""
          int WordCount ""
          bit TableOfContents ""
          
}
"dbo.OrganizationalUnit" {
    int Id "PK"
          nvarchar(255) Email ""
          nvarchar(255) Phone ""
          nvarchar(255) Address ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.ActivityVersion" {
    int Activity_Id "PK, FK"
          int Lcid "PK"
          int VersionNumber "PK"
          nvarchar(255) Title ""
          nvarchar(-1) Message ""
          datetime Created ""
          int ContentId ""
          int CreatedById "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.PageTemplate" {
    int Id "PK"
          nvarchar(255) Title ""
          datetime Created ""
          int Layout_id "FK"
          
}
"dbo.ConfigurationSetting" {
    nvarchar(255) Name "PK"
          nvarchar(-1) Value ""
          
}
"dbo.Praises" {
    int Activity_id "FK, PK"
          int User_id "FK, PK"
          nvarchar(255) SelectedBadge ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.CorporateTreeNode" {
    int Id "PK"
          nvarchar(255) Type ""
          nvarchar(450) Path ""
          nvarchar(255) Title ""
          nvarchar(340) Description ""
          nvarchar(255) ImageUrl ""
          int UIOrder ""
          nvarchar(255) Status ""
          int CorporateSiteId "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.RelatedGroups" {
    int SourceGroupId "FK, PK"
          int TargetGroupId "FK, PK"
          
}
"dbo.CorporateTreeNodeTranslation" {
    int Id "PK"
          nvarchar(255) Title ""
          nvarchar(340) Description ""
          int LCID ""
          int NodeId "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.Rule" {
    int Id "PK"
          int ParentRule_id "FK"
          
}
"dbo.DataClassification" {
    int Id "PK"
          nvarchar(255) Title ""
          nvarchar(255) Description ""
          nvarchar(255) Tooltip ""
          nvarchar(255) Link ""
          bit IsHiddenDefault ""
          bit IsModeratedDefault ""
          bit IsPrivateDefault ""
          bit IsPublicDefault ""
          
}
"dbo.RuleDomainGroup" {
    int DomainGroupRule_id "FK, PK"
          bit MemberOf ""
          int DomainGroup_id "FK"
          
}
"dbo.DirectoryContent" {
    int Id "PK"
          int Type ""
          int Group_id "FK"
          nvarchar(255) Name ""
          nvarchar(2048) Url ""
          int Attachment_Id "FK"
          int ParentFolderId "FK"
          nvarchar(500) Path ""
          bit IsDeleted ""
          datetime Deleted ""
          uniqueidentifier ListGuid ""
          int ItemId ""
          
}
"dbo.RuleSet" {
    int RuleSet_id "FK, PK"
          nvarchar(255) Operator ""
          
}
"ContentStorage.BlogPostVersion" {
    int ContentId "PK"
          nvarchar(-1) Title ""
          nvarchar(-1) Body ""
          nvarchar(-1) BodyMetadata ""
          
}
"dbo.DiscoveryCard" {
    int Id "PK"
          varchar(50) CardType ""
          int LocalEntity_id "FK"
          bit Active ""
          int Author_id "FK"
          datetime Created ""
          datetime LastActive ""
          nvarchar(255) Title ""
          nvarchar(255) Image ""
          
}
"dbo.RuleUser" {
    int RuleUser_id "FK, PK"
          int User_id "FK"
          
}
"dbo.DiscoveryCardConfiguration" {
    int DiscoveryCard_id "PK, FK"
          int LocalEntity_id "PK, FK"
          nvarchar(-1) Configuration ""
          
}
"dbo.DomainGroup" {
    int Id "PK"
          nvarchar(255) Name ""
          nvarchar(255) InternalId ""
          datetime Updated ""
          bit IsDeleted ""
          
}
"dbo.RuleUserProperty" {
    int UserPropertyRule_id "FK, PK"
          nvarchar(255) PropertyName ""
          nvarchar(255) Operator ""
          nvarchar(255) TargetValue ""
          float TargetValueNumber ""
          
}
"dbo.Scope" {
    int Id "PK"
          nvarchar(255) Name ""
          
}
"dbo.EmailQueue" {
    int ItemId "PK"
          datetime Created ""
          datetime LastPeek ""
          nvarchar(-1) Item ""
          nvarchar(4000) Type ""
          
}
"dbo.ExtendedIdeaDetail" {
    int ActivityId "PK, FK"
          nvarchar(255) State ""
          bit Implemented ""
          nvarchar(-1) RefinementData ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.SecuredActivityUser" {
    int User_id "FK, PK"
          int SecuredActivity_id "FK, PK"
          
}
"dbo.ExtendedIdeaRelatedCommunity" {
    int ExtendedIdeaDetail_id "PK, FK"
          int Group_id "PK, FK"
          
}
"dbo.ShareAppDetail" {
    int ShareId "FK, PK"
          int SharedApp_id "FK"
          
}
"dbo.ExtendedIdeaTeamMember" {
    int ExtendedIdeaDetail_id "PK, FK"
          int User_id "PK, FK"
          
}
"dbo.ShareDetail" {
    int ShareId "FK, PK"
          int SharedActivity_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.FeatureSetting" {
    int Id "PK"
          nvarchar(-1) Setting ""
          
}
"dbo.SiteCollection" {
    int Id "PK"
          uniqueidentifier SiteCollectionId ""
          nvarchar(255) WebApplicationId ""
          nvarchar(255) SiteCollectionUrl ""
          nvarchar(255) WebApplicationUrl ""
          bit IsRoot ""
          bit IsCommunityCreation ""
          bit IsWikiCreation ""
          bit IsBlogCreation ""
          bit IsKnowledgeCenterCreation ""
          bit IsCorporateSiteCreation ""
          nvarchar(255) Version ""
          nvarchar(255) Status ""
          bit Enabled ""
          bit IsIdeasCampaignCreation ""
          
}
"dbo.FollowedNotification" {
    int Id "PK"
          bit IsRead ""
          int UserId "FK"
          int HashtagId "FK"
          int ActivityId "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"ContentStorage.WikiPageVersion" {
    int ContentId "PK"
          nvarchar(-1) Title ""
          nvarchar(-1) Body ""
          nvarchar(-1) BodyMetadata ""
          
}
"dbo.Followers" {
    int Activity_id "PK, FK"
          int User_id "PK, FK"
          
}
"ContentStorage.QuestionVersion" {
    int ContentId "PK"
          nvarchar(-1) Title ""
          nvarchar(-1) Body ""
          nvarchar(-1) BodyMetadata ""
          
}
"dbo.Skills" {
    int Id "PK"
          nvarchar(255) Name ""
          datetime Created ""
          
}
"dbo.Group" {
    int GroupId "PK"
          nvarchar(255) GroupType ""
          nvarchar(255) Title ""
          nvarchar(2048) Description ""
          datetime Created ""
          datetime Updated ""
          nvarchar(255) Url ""
          bit IsPublic ""
          bit IsModerated ""
          bit ReadOnly ""
          bit IsDiscoverable ""
          datetime Archive ""
          uniqueidentifier WebId ""
          nvarchar(255) Color ""
          nvarchar(255) BannerUrl ""
          nvarchar(255) LogoUrl ""
          nvarchar(255) TimeZone ""
          int SiteCollectionId "FK"
          int DataClassification_id "FK"
          int ParentGroupId "FK"
          bit TermsRequired ""
          int OrganizationalUnitId "FK"
          datetime SubmissionDeadlineDate ""
          datetime ImpactAnnouncementDate ""
          int LocalEntity_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.Tags" {
    int Group_id "FK, PK"
          int HashTag_id "FK, PK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.WebHookConnector" {
    int Id "PK"
          uniqueidentifier Connector_id ""
          nvarchar(2048) WebHookConnectorUrl ""
          char(64) Secret ""
          bit IsActive ""
          datetime Created ""
          datetime LastTriggered ""
          int CurrentUser_id "FK"
          
}
"dbo.GroupDisplayChannel" {
    int PlaceId "PK, FK"
          int ChannelId "PK, FK"
          
}
"HangFire.Schema" {
    int Version "PK"
          
}
"dbo.TeamPosition" {
    int Id "PK"
          nvarchar(255) Responsibility ""
          int UIOrder ""
          int OrganizationalUnitId "FK"
          int SectionId "FK"
          int UserId "FK"
          
}
"dbo.GroupDisplayPage" {
    int PlaceId "PK, FK"
          int PageId "PK, FK"
          bit UIRelevant ""
          int UIOrder ""
          
}
"HangFire.Job" {
    int Id "PK"
          int StateId ""
          nvarchar(20) StateName ""
          nvarchar(-1) InvocationData ""
          nvarchar(-1) Arguments ""
          datetime CreatedAt ""
          datetime ExpireAt ""
          
}
"dbo.TeamSection" {
    int Id "PK"
          nvarchar(255) Title ""
          int UIOrder ""
          int OrganizationalUnitId "FK"
          
}
"dbo.WebHookConnectorChannel" {
    int WebHookConnector_id "PK, FK"
          int Channel_id "PK"
          
}
"dbo.GroupDomainGroup" {
    int Group_id "PK, FK"
          int DomainGroup_id "PK, FK"
          
}
"HangFire.State" {
    int Id "PK"
          int JobId "FK"
          nvarchar(20) Name ""
          nvarchar(100) Reason ""
          datetime CreatedAt ""
          nvarchar(-1) Data ""
          
}
"dbo.TeamSectionTranslation" {
    int Section_Id "FK, PK"
          int Lcid "PK"
          nvarchar(255) Title ""
          
}
"dbo.GroupEmailDigestSubscriber" {
    int User_id "PK, FK"
          int Group_id "PK, FK"
          int Type "PK"
          datetime SubscriberSince ""
          
}
"dbo.WebHookEvent" {
    int Id "PK"
          uniqueidentifier Event_id ""
          int WebHookConnector_id "FK"
          int Content_id ""
          nvarchar(255) ContentType ""
          nvarchar(1024) ContentLanguages ""
          nvarchar(255) EventType ""
          nvarchar(255) SiteCollectionUrl ""
          datetime Created ""
          
}
"HangFire.JobParameter" {
    int Id "PK"
          int JobId "FK"
          nvarchar(40) Name ""
          nvarchar(-1) Value ""
          
}
"dbo.Term" {
    int Id "PK"
          nvarchar(255) Name ""
          nvarchar(255) Guid ""
          int TermSet_id "FK"
          
}
"dbo.GroupFeed" {
    int Id "PK"
          nvarchar(2048) Url ""
          int Count ""
          int Group_id "FK"
          
}
"dbo.TermSet" {
    int Id "PK"
          nvarchar(255) Name ""
          nvarchar(255) TermGroup ""
          nvarchar(255) Guid ""
          
}
"dbo.GroupFollower" {
    int Group_id "FK"
          int User_id "FK"
          int Id "PK"
          datetime FollowerSince ""
          bit IsFromDomainGroup ""
          tinyint Role ""
          bit UIRelevant ""
          bit IsFromAudience ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"HangFire.JobQueue" {
    int Id "PK"
          int JobId ""
          nvarchar(50) Queue ""
          datetime FetchedAt ""
          
}
"dbo.WebHookPendingNotification" {
    int Id "PK"
          int WebHookEvent_id "FK"
          datetime LastTriggered ""
          int RetryNumber ""
          
}
"dbo.TranslationSkeleton" {
    int Id "PK"
          nvarchar(255) SkeletonFileName ""
          nvarchar(-1) Content ""
          int Activity_id "FK"
          
}
"dbo.GroupInvitation" {
    int Id "PK"
          datetime Created ""
          tinyint Role ""
          int User_id "FK"
          int Group_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"HangFire.Server" {
    nvarchar(100) Id "PK"
          nvarchar(-1) Data ""
          datetime LastHeartbeat ""
          
}
"dbo.EventFiringSwitch" {
    uniqueidentifier CorrelationId "PK"
          timestamp Created ""
          
}
"dbo.WebHookFinishedNotification" {
    int Id "PK"
          int WebHookEvent_id "FK"
          datetime LastTriggered ""
          int RetryNumber ""
          bit Success ""
          
}
"dbo.GroupMembershipRequest" {
    int Id "PK"
          tinyint Role ""
          nvarchar(255) Message ""
          datetime Created ""
          int Group_id "FK"
          int User_id "FK"
          
}
"dbo.User" {
    int Id "PK"
          nvarchar(255) FullName ""
          nvarchar(255) PictureUrl ""
          nvarchar(255) BackgroundPictureUrl ""
          int BackgroundPictureOffsetX ""
          int BackgroundPictureOffsetY ""
          nvarchar(255) SipAddress ""
          nvarchar(255) Email ""
          bit EulaAccepted ""
          bit EulaRejected ""
          bit AdditionalEulaAccepted ""
          nvarchar(255) LoginName ""
          bit IsActive ""
          bit IsReadOnly ""
          bit SubscribedToEmailNotifications ""
          nvarchar(-1) AboutMe ""
          nvarchar(255) WorkPhone ""
          nvarchar(255) Title ""
          nvarchar(255) JobTitle ""
          nvarchar(255) Office ""
          nvarchar(255) OfficeLocation ""
          nvarchar(255) Department ""
          datetime LastUpdated ""
          datetime Joined ""
          int LocaleId ""
          nvarchar(255) SID ""
          bit IsRegulated ""
          
}
"dbo.GroupPage" {
    int Id "PK"
          nvarchar(255) GroupPageType ""
          nvarchar(255) Name ""
          datetime Created ""
          bit IsCustomized ""
          int LCID ""
          int Layout_id "FK"
          int PageTemplate_id "FK"
          int Group_id "FK"
          nvarchar(255) Description ""
          nvarchar(255) Url ""
          nvarchar(255) ListGuid ""
          int ItemId ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"HangFire.List" {
    int Id "PK"
          nvarchar(100) Key ""
          nvarchar(-1) Value ""
          datetime ExpireAt ""
          
}
"dbo.UserDomainGroup" {
    int User_id "FK, PK"
          int DomainGroup_id "FK, PK"
          
}
"dbo.GroupPageTranslation" {
    int Id "PK"
          int LCID ""
          int GroupPage_id "FK"
          
}
"HangFire.Set" {
    int Id "PK"
          nvarchar(100) Key ""
          float Score ""
          nvarchar(256) Value ""
          datetime ExpireAt ""
          
}
"dbo.UserDynamicProperty" {
    int Id "PK"
          nvarchar(255) Property ""
          nvarchar(255) Value ""
          int User_id "FK"
          
}
"dbo.GroupTermset" {
    int Group_id "PK, FK"
          int TermSet_id "PK, FK"
          
}
"dbo.UserEndorsements" {
    int UserSkill_id "FK, PK"
          int User_id "FK, PK"
          datetime Created ""
          
}
"dbo.GroupTools" {
    int Id "PK"
          nvarchar(255) Title ""
          datetime Created ""
          nvarchar(255) Type ""
          nvarchar(255) Url ""
          nvarchar(255) ListGuid ""
          nvarchar(255) Folder ""
          bit Active ""
          bit ReadOnly ""
          nvarchar(-1) Configuration ""
          int Group_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"HangFire.Counter" {
    int Id "PK"
          nvarchar(100) Key ""
          smallint Value ""
          datetime ExpireAt ""
          
}
"dbo.UserExternalTask" {
    int User_id "FK, PK"
          int Activity_id "FK, PK"
          
}
"dbo.GroupTranslation" {
    int Id "PK"
          nvarchar(255) Title ""
          nvarchar(340) Description ""
          int LCID ""
          int GroupId "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"HangFire.Hash" {
    int Id "PK"
          nvarchar(100) Key ""
          nvarchar(100) Field ""
          nvarchar(-1) Value ""
          datetime2 ExpireAt ""
          
}
"dbo.ChannelDomainGroup" {
    int DomainGroup_id "PK, FK"
          int Channel_id "PK, FK"
          
}
"dbo.UserFollowedHashTag" {
    int HashTag_id "FK, PK"
          int User_id "FK, PK"
          int Scope_id "FK, PK"
          datetime Created ""
          
}
"dbo.GroupViewer" {
    int Group_id "FK"
          int User_id "FK"
          int Id "PK"
          datetime ViewerSince ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"HangFire.AggregatedCounter" {
    int Id "PK"
          nvarchar(100) Key ""
          bigint Value ""
          datetime ExpireAt ""
          
}
"dbo.UserFollowedLanguages" {
    int Language_id "FK, PK"
          int User_id "FK, PK"
          
}
"dbo.HashTag" {
    int Id "PK"
          uniqueidentifier MetadataId ""
          nvarchar(255) Name ""
          int Trending ""
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.ChannelEditor" {
    int User_id "PK, FK"
          int Channel_id "PK, FK"
          
}
"ContentStorage.PageVersion" {
    int ContentId "PK"
          nvarchar(-1) Title ""
          nvarchar(-1) Body ""
          nvarchar(-1) BodyMetadata ""
          
}
"dbo.UserFollower" {
    int FollowerUser_id "FK, PK"
          int FollowedUser_id "FK, PK"
          datetime FollowerSince ""
          
}
"dbo.HashTaggedActivity" {
    int Id "PK"
          int Activity_id "FK"
          int Comment_id "FK"
          int HashTag_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"ContentStorage.StoryVersion" {
    int ContentId "PK"
          nvarchar(-1) Title ""
          nvarchar(-1) Body ""
          nvarchar(-1) BodyMetadata ""
          
}
"dbo.UserGroupContribution" {
    int Id "PK"
          int ContributionPoints ""
          int User_id "FK"
          int Group_id "FK"
          
}
"dbo.HashtaggedApp" {
    int App_id "FK, PK"
          int HashTag_id "FK, PK"
          
}
"dbo.Activity" {
    int Id "PK"
          nvarchar(255) Type ""
          nvarchar(-1) Message ""
          datetime Created ""
          datetime LastModified ""
          nvarchar(255) Device ""
          smallint Visibility ""
          datetime InformationalDateTime ""
          datetime InformationalDateTime2 ""
          nvarchar(255) InformationalText ""
          nvarchar(255) Title ""
          int Views ""
          bit Highlighted ""
          int InformationalNumber1 ""
          int InformationalNumber2 ""
          nvarchar(255) Version ""
          int LCID ""
          int Group_id "FK"
          int Tool_id "FK"
          int User_id "FK"
          int InformationalUser_id "FK"
          int LastEditor_id "FK"
          nvarchar(255) Description ""
          nvarchar(2048) Url ""
          nvarchar(255) ListGuid ""
          int ItemId ""
          int Views_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.HashTaggedGroup" {
    int Id "PK"
          int Group_id "FK"
          int HashTag_id "FK"
          bit IsDeleted ""
          datetime Deleted ""
          
}
"dbo.ActivityImageCropping" {
    int ActivityId "FK, PK"
          varchar(30) ImageCroppingId "PK"
          decimal Zoom ""
          int OffsetX ""
          int OffsetY ""
          int Width ""
          int Height ""
          
}
"dbo.HeroBlock" {
    int Id "PK"
          int HeroBlockTemplate_id "FK"
          bit IsDefault ""
          nvarchar(255) Type ""
          bit IsPublished ""
          nvarchar(255) Title ""
          nvarchar(255) SubTitle ""
          nvarchar(2000) Description ""
          nvarchar(2000) SourceUrl ""
          nvarchar(2000) ImageUrl ""
          nvarchar(2000) AutoselectedImageUrl ""
          nvarchar(255) LinkType ""
          nvarchar(2000) LinkUrl ""
          nvarchar(2000) VideoUrl ""
          bit LinkInNewWindow ""
          nvarchar(255) IconType ""
          nvarchar(255) StorySource ""
          int NumberOfStories ""
          bit OnlyFeatured ""
          nvarchar(255) BackgroundType ""
          nvarchar(255) BackgroundColor ""
          nvarchar(255) SubType ""
          bit IsEnabled ""
          datetime StartDate ""
          datetime EndDate ""
          bit PendingDelete ""
          bit AutoPlay ""
          bit AllowRestrictedChannels ""
          
}
"dbo.UserPropertyBag" {
    int UserId "FK, PK"
          varchar(25) PropertyId "PK"
          varchar(255) PropertyType ""
          nvarchar(-1) PropertyValue ""
          
}
"dbo.ActivityLikes" {
    int Activity_id "FK, PK"
          int User_id "FK, PK"
          datetime Created ""
          
}
"dbo.HeroBlockChannel" {
    int HeroBlock_id "FK, PK"
          int Channel_id "FK, PK"
          
}
"dbo.UserSection" {
    int Id "PK"
          nvarchar(255) Title ""
          int SectionOrder ""
          int User_id "FK"
          
}
      "dbo.ActivityMessageContent" ||--|{ "dbo.Activity": "Id"
"dbo.UserSkills" |o--|{ "dbo.User": "Id"
"dbo.UserSkills" |o--|{ "dbo.Skills": "Id"
"dbo.ActivityMetadataProperty" |o--|{ "dbo.Activity": "Id"
"dbo.HeroBlockTranslation" ||--|{ "dbo.HeroBlock": "Id"
"dbo.UserToNotification" ||--|{ "dbo.Notification": "Id"
"dbo.UserToNotification" ||--|{ "dbo.User": "Id"
"dbo.ActivityReports" |o--|{ "dbo.Activity": "Id"
"dbo.ActivityReports" |o--|{ "dbo.Comment": "Id"
"dbo.ActivityReports" |o--|{ "dbo.User": "Id"
"dbo.ZoneInstance" |o--|{ "dbo.PageTemplate": "Id"
"dbo.ZoneInstance" |o--|{ "dbo.LayoutZone": "Id"
"dbo.ZoneInstance" |o--|{ "dbo.GroupPage": "Id"
"dbo.ZoneInstance" |o--|{ "dbo.GroupPageTranslation": "Id"
"dbo.ActivityTerm" ||--|{ "dbo.Activity": "Id"
"dbo.ActivityTerm" ||--|{ "dbo.Term": "Id"
"dbo.HeroTemplateBlockTemplate" ||--|{ "dbo.HeroTemplate": "Id"
"dbo.HeroTemplateBlockTemplate" ||--|{ "dbo.HeroBlockTemplate": "Id"
"dbo.ActivityTranslation" |o--|{ "dbo.Activity": "Id"
"dbo.HeroWidgetBlockContent" ||--|{ "dbo.HeroBlock": "Id"
"dbo.ActivityUserSection" ||--|{ "dbo.Activity": "Id"
"dbo.ActivityUserSection" ||--|{ "dbo.UserSection": "Id"
"dbo.AllowedModules" |o--|{ "dbo.LayoutZone": "Id"
"dbo.LayoutZone" |o--|{ "dbo.Layout": "Id"
"dbo.App" |o--|{ "dbo.LocalEntity": "Id"
"dbo.AppCategory" |o--|{ "dbo.LocalEntity": "Id"
"dbo.AppCategoryApp" ||--|{ "dbo.App": "Id"
"dbo.AppCategoryApp" ||--|{ "dbo.AppCategory": "Id"
"dbo.LocalEntityDomainGroup" ||--|{ "dbo.DomainGroup": "Id"
"dbo.LocalEntityDomainGroup" ||--|{ "dbo.LocalEntity": "Id"
"dbo.AppCategoryTranslation" ||--|{ "dbo.AppCategory": "Id"
"dbo.LocalEntityHeroBlock" ||--|{ "dbo.HeroBlock": "Id"
"dbo.LocalEntityHeroBlock" ||--|{ "dbo.LocalEntity": "Id"
"dbo.AppResponsible" ||--|{ "dbo.App": "Id"
"dbo.AppResponsible" ||--|{ "dbo.User": "Id"
"dbo.GroupAudience" ||--|{ "dbo.Group": "GroupId"
"dbo.GroupAudience" ||--|{ "dbo.Audience": "Id"
"dbo.LocalEntityHeroTemplate" ||--|{ "dbo.HeroTemplate": "Id"
"dbo.LocalEntityHeroTemplate" ||--|{ "dbo.LocalEntity": "Id"
"dbo.AppScreenshot" ||--|{ "dbo.App": "Id"
"dbo.LocalEntityMember" ||--|{ "dbo.User": "Id"
"dbo.LocalEntityMember" ||--|{ "dbo.LocalEntity": "Id"
"dbo.AppTranslation" ||--|{ "dbo.App": "Id"
"dbo.LocalEntityMenuNode" ||--|{ "dbo.MenuNode": "Id"
"dbo.LocalEntityMenuNode" ||--|{ "dbo.LocalEntity": "Id"
"dbo.AppUser" ||--|{ "dbo.App": "Id"
"dbo.AppUser" ||--|{ "dbo.User": "Id"
"dbo.Mentions" ||--|{ "dbo.Activity": "Id"
"dbo.Mentions" ||--|{ "dbo.User": "Id"
"dbo.AccessManagementUser" ||--|| "dbo.User": "Id"
"dbo.Attachment" |o--|{ "dbo.Activity": "Id"
"dbo.Attachment" |o--|{ "dbo.User": "Id"
"dbo.Attachment" |o--|{ "dbo.User": "Id"
"dbo.MenuItem" |o--|{ "dbo.MenuSection": "Id"
"dbo.Audience" |o--|{ "dbo.AudienceCategory": "Id"
"dbo.Audience" |o--|{ "dbo.Audience": "Id"
"dbo.Audience" |o--|{ "dbo.Rule": "Id"
"dbo.MenuItemTranslation" |o--|{ "dbo.MenuItem": "Id"
"dbo.AccessManagementDomainGroup" ||--|| "dbo.DomainGroup": "Id"
"dbo.AudienceUser" ||--|{ "dbo.Audience": "Id"
"dbo.AudienceUser" ||--|{ "dbo.User": "Id"
"dbo.MenuNodeSection" ||--|{ "dbo.MenuNode": "Id"
"dbo.MenuNodeSection" ||--|{ "dbo.MenuSection": "Id"
"dbo.RbacUser" ||--|| "dbo.User": "Id"
"dbo.Bookmarks" ||--|{ "dbo.Activity": "Id"
"dbo.Bookmarks" ||--|{ "dbo.User": "Id"
"dbo.MenuNodeTranslation" |o--|{ "dbo.MenuNode": "Id"
"dbo.Channel" ||--|{ "dbo.ChannelCategory": "Id"
"dbo.Channel" ||--|{ "dbo.Group": "GroupId"
"dbo.ChannelAudience" ||--|{ "dbo.Audience": "Id"
"dbo.ChannelAudience" ||--|{ "dbo.Channel": "Id"
"dbo.ChannelCategory" ||--|{ "dbo.Group": "GroupId"
"dbo.LocalEntityAdmin" ||--|{ "dbo.User": "Id"
"dbo.LocalEntityAdmin" ||--|{ "dbo.LocalEntity": "Id"
"dbo.MenuSectionMetadataProperty" |o--|{ "dbo.MenuSection": "Id"
"dbo.ChannelFollow" ||--|{ "dbo.User": "Id"
"dbo.ChannelFollow" ||--|{ "dbo.Channel": "Id"
"dbo.MenuSectionTranslation" |o--|{ "dbo.MenuSection": "Id"
"dbo.ChannelOwner" ||--|{ "dbo.Channel": "Id"
"dbo.ChannelOwner" ||--|{ "dbo.User": "Id"
"dbo.ModuleInstance" |o--|{ "dbo.ZoneInstance": "Id"
"dbo.Comment" |o--|{ "dbo.Activity": "Id"
"dbo.Comment" |o--|{ "dbo.User": "Id"
"dbo.Comment" |o--|{ "dbo.User": "Id"
"dbo.MyItemsCategory" ||--|{ "dbo.User": "Id"
"dbo.MyItemsCategory" ||--|{ "dbo.Group": "GroupId"
"dbo.CommentLikes" ||--|{ "dbo.Comment": "Id"
"dbo.CommentLikes" ||--|{ "dbo.User": "Id"
"dbo.MyItemsCategoryCommunicationPage" ||--|{ "dbo.MyItemsCategory": "Id"
"dbo.MyItemsCategoryCommunicationPage" ||--|{ "dbo.CommunicationPageDetail": "ActivityId"
"dbo.MyItemsCategoryCommunicationPage" |o--|{ "dbo.MyItemsCategoryCommunicationPage": "Category"
"dbo.MyItemsCategoryCommunicationPage" |o--|{ "dbo.MyItemsCategoryCommunicationPage": "CommunicationPage"
"dbo.MyItemsCategoryCommunicationPage" |o--|{ "dbo.MyItemsCategoryCommunicationPage": "Category"
"dbo.MyItemsCategoryCommunicationPage" |o--|{ "dbo.MyItemsCategoryCommunicationPage": "CommunicationPage"
"dbo.CommunicationPageAction" ||--|{ "dbo.CommunicationPageDetail": "ActivityId"
"dbo.CommunicationPageAction" ||--|{ "dbo.User": "Id"
"dbo.CommunicationPageAction" |o--|{ "dbo.CommunicationPageAction": "Id"
"dbo.CommunicationPageAuthor" ||--|{ "dbo.User": "Id"
"dbo.CommunicationPageAuthor" ||--|{ "dbo.CommunicationPageDetail": "ActivityId"
"dbo.CommunicationPageChannel" ||--|{ "dbo.Channel": "Id"
"dbo.CommunicationPageChannel" ||--|{ "dbo.CommunicationPageDetail": "ActivityId"
"dbo.Notification" |o--|{ "dbo.Activity": "Id"
"dbo.Notification" |o--|{ "dbo.Group": "GroupId"
"dbo.Notification" |o--|{ "dbo.User": "Id"
"dbo.Notification" |o--|{ "dbo.App": "Id"
"dbo.CommunicationPageDetail" ||--|{ "dbo.Activity": "Id"
"dbo.ActivityVersion" ||--|{ "dbo.Activity": "Id"
"dbo.ActivityVersion" ||--|{ "dbo.User": "Id"
"dbo.PageTemplate" |o--|{ "dbo.Layout": "Id"
"dbo.Praises" ||--|{ "dbo.Activity": "Id"
"dbo.Praises" ||--|{ "dbo.User": "Id"
"dbo.CorporateTreeNode" |o--|{ "dbo.Group": "GroupId"
"dbo.RelatedGroups" ||--|{ "dbo.Group": "GroupId"
"dbo.RelatedGroups" ||--|{ "dbo.Group": "GroupId"
"dbo.CorporateTreeNodeTranslation" ||--|{ "dbo.CorporateTreeNode": "Id"
"dbo.Rule" |o--|{ "dbo.RuleSet": "RuleSet_id"
"dbo.RuleDomainGroup" ||--|{ "dbo.Rule": "Id"
"dbo.RuleDomainGroup" |o--|{ "dbo.DomainGroup": "Id"
"dbo.DirectoryContent" ||--|{ "dbo.Group": "GroupId"
"dbo.DirectoryContent" |o--|{ "dbo.Attachment": "Id"
"dbo.DirectoryContent" |o--|{ "dbo.DirectoryContent": "Id"
"dbo.RuleSet" ||--|{ "dbo.Rule": "Id"
"dbo.DiscoveryCard" ||--|{ "dbo.LocalEntity": "Id"
"dbo.DiscoveryCard" |o--|{ "dbo.User": "Id"
"dbo.RuleUser" ||--|{ "dbo.Rule": "Id"
"dbo.RuleUser" |o--|{ "dbo.User": "Id"
"dbo.DiscoveryCardConfiguration" ||--|{ "dbo.DiscoveryCard": "Id"
"dbo.DiscoveryCardConfiguration" ||--|{ "dbo.LocalEntity": "Id"
"dbo.RuleUserProperty" ||--|{ "dbo.Rule": "Id"
"dbo.ExtendedIdeaDetail" ||--|{ "dbo.Activity": "Id"
"dbo.SecuredActivityUser" ||--|{ "dbo.User": "Id"
"dbo.SecuredActivityUser" ||--|{ "dbo.Activity": "Id"
"dbo.ExtendedIdeaRelatedCommunity" ||--|{ "dbo.ExtendedIdeaDetail": "ActivityId"
"dbo.ExtendedIdeaRelatedCommunity" ||--|{ "dbo.Group": "GroupId"
"dbo.ShareAppDetail" ||--|{ "dbo.Activity": "Id"
"dbo.ShareAppDetail" |o--|{ "dbo.App": "Id"
"dbo.ExtendedIdeaTeamMember" ||--|{ "dbo.ExtendedIdeaDetail": "ActivityId"
"dbo.ExtendedIdeaTeamMember" ||--|{ "dbo.User": "Id"
"dbo.ShareDetail" ||--|{ "dbo.Activity": "Id"
"dbo.ShareDetail" |o--|{ "dbo.Activity": "Id"
"dbo.FollowedNotification" |o--|{ "dbo.User": "Id"
"dbo.FollowedNotification" |o--|{ "dbo.HashTag": "Id"
"dbo.FollowedNotification" |o--|{ "dbo.Activity": "Id"
"dbo.Followers" ||--|{ "dbo.Activity": "Id"
"dbo.Followers" ||--|{ "dbo.User": "Id"
"dbo.Group" |o--|{ "dbo.SiteCollection": "Id"
"dbo.Group" |o--|{ "dbo.DataClassification": "Id"
"dbo.Group" |o--|{ "dbo.Group": "GroupId"
"dbo.Group" |o--|{ "dbo.OrganizationalUnit": "Id"
"dbo.Group" |o--|{ "dbo.LocalEntity": "Id"
"dbo.Tags" ||--|{ "dbo.Group": "GroupId"
"dbo.Tags" ||--|{ "dbo.HashTag": "Id"
"dbo.WebHookConnector" ||--|{ "dbo.User": "Id"
"dbo.GroupDisplayChannel" ||--|{ "dbo.Group": "GroupId"
"dbo.GroupDisplayChannel" ||--|{ "dbo.Channel": "Id"
"dbo.TeamPosition" ||--|{ "dbo.OrganizationalUnit": "Id"
"dbo.TeamPosition" ||--|{ "dbo.TeamSection": "Id"
"dbo.TeamPosition" ||--|{ "dbo.User": "Id"
"dbo.GroupDisplayPage" ||--|{ "dbo.Group": "GroupId"
"dbo.GroupDisplayPage" ||--|{ "dbo.Activity": "Id"
"dbo.TeamSection" ||--|{ "dbo.OrganizationalUnit": "Id"
"dbo.WebHookConnectorChannel" ||--|{ "dbo.WebHookConnector": "Id"
"dbo.GroupDomainGroup" ||--|{ "dbo.Group": "GroupId"
"dbo.GroupDomainGroup" ||--|{ "dbo.DomainGroup": "Id"
"HangFire.State" ||--|{ "HangFire.Job": "Id"
"dbo.TeamSectionTranslation" ||--|{ "dbo.TeamSection": "Id"
"dbo.GroupEmailDigestSubscriber" ||--|{ "dbo.User": "Id"
"dbo.GroupEmailDigestSubscriber" ||--|{ "dbo.Group": "GroupId"
"dbo.WebHookEvent" ||--|{ "dbo.WebHookConnector": "Id"
"HangFire.JobParameter" ||--|{ "HangFire.Job": "Id"
"dbo.Term" |o--|{ "dbo.TermSet": "Id"
"dbo.GroupFeed" |o--|{ "dbo.Group": "GroupId"
"dbo.GroupFollower" |o--|{ "dbo.Group": "GroupId"
"dbo.GroupFollower" |o--|{ "dbo.User": "Id"
"dbo.WebHookPendingNotification" ||--|{ "dbo.WebHookEvent": "Id"
"dbo.TranslationSkeleton" |o--|{ "dbo.Activity": "Id"
"dbo.GroupInvitation" |o--|{ "dbo.User": "Id"
"dbo.GroupInvitation" |o--|{ "dbo.Group": "GroupId"
"dbo.WebHookFinishedNotification" ||--|{ "dbo.WebHookEvent": "Id"
"dbo.GroupMembershipRequest" |o--|{ "dbo.Group": "GroupId"
"dbo.GroupMembershipRequest" |o--|{ "dbo.User": "Id"
"dbo.GroupPage" |o--|{ "dbo.Layout": "Id"
"dbo.GroupPage" |o--|{ "dbo.PageTemplate": "Id"
"dbo.GroupPage" |o--|{ "dbo.Group": "GroupId"
"dbo.UserDomainGroup" ||--|{ "dbo.User": "Id"
"dbo.UserDomainGroup" ||--|{ "dbo.DomainGroup": "Id"
"dbo.GroupPageTranslation" |o--|{ "dbo.GroupPage": "Id"
"dbo.UserDynamicProperty" |o--|{ "dbo.User": "Id"
"dbo.GroupTermset" ||--|{ "dbo.Group": "GroupId"
"dbo.GroupTermset" ||--|{ "dbo.TermSet": "Id"
"dbo.UserEndorsements" ||--|{ "dbo.UserSkills": "Id"
"dbo.UserEndorsements" ||--|{ "dbo.User": "Id"
"dbo.GroupTools" |o--|{ "dbo.Group": "GroupId"
"dbo.UserExternalTask" ||--|{ "dbo.User": "Id"
"dbo.UserExternalTask" ||--|{ "dbo.Activity": "Id"
"dbo.GroupTranslation" ||--|{ "dbo.Group": "GroupId"
"dbo.ChannelDomainGroup" ||--|{ "dbo.DomainGroup": "Id"
"dbo.ChannelDomainGroup" ||--|{ "dbo.Channel": "Id"
"dbo.UserFollowedHashTag" ||--|{ "dbo.HashTag": "Id"
"dbo.UserFollowedHashTag" ||--|{ "dbo.User": "Id"
"dbo.UserFollowedHashTag" ||--|{ "dbo.Scope": "Id"
"dbo.GroupViewer" |o--|{ "dbo.Group": "GroupId"
"dbo.GroupViewer" |o--|{ "dbo.User": "Id"
"dbo.UserFollowedLanguages" ||--|{ "dbo.Language": "LCID"
"dbo.UserFollowedLanguages" ||--|{ "dbo.User": "Id"
"dbo.ChannelEditor" ||--|{ "dbo.User": "Id"
"dbo.ChannelEditor" ||--|{ "dbo.Channel": "Id"
"dbo.UserFollower" ||--|{ "dbo.User": "Id"
"dbo.UserFollower" ||--|{ "dbo.User": "Id"
"dbo.HashTaggedActivity" |o--|{ "dbo.Activity": "Id"
"dbo.HashTaggedActivity" |o--|{ "dbo.Comment": "Id"
"dbo.HashTaggedActivity" |o--|{ "dbo.HashTag": "Id"
"dbo.UserGroupContribution" ||--|| "dbo.User": "Id"
"dbo.UserGroupContribution" ||--|| "dbo.Group": "GroupId"
"dbo.HashtaggedApp" ||--|{ "dbo.App": "Id"
"dbo.HashtaggedApp" ||--|{ "dbo.HashTag": "Id"
"dbo.Activity" |o--|{ "dbo.Group": "GroupId"
"dbo.Activity" |o--|{ "dbo.GroupTools": "Id"
"dbo.Activity" |o--|{ "dbo.User": "Id"
"dbo.Activity" |o--|{ "dbo.User": "Id"
"dbo.Activity" |o--|{ "dbo.User": "Id"
"dbo.Activity" |o--|{ "dbo.ActivityViews": "Id"
"dbo.HashTaggedGroup" |o--|{ "dbo.Group": "GroupId"
"dbo.HashTaggedGroup" |o--|{ "dbo.HashTag": "Id"
"dbo.ActivityImageCropping" ||--|{ "dbo.Activity": "Id"
"dbo.HeroBlock" ||--|{ "dbo.HeroBlockTemplate": "Id"
"dbo.UserPropertyBag" ||--|{ "dbo.User": "Id"
"dbo.ActivityLikes" ||--|{ "dbo.Activity": "Id"
"dbo.ActivityLikes" ||--|{ "dbo.User": "Id"
"dbo.HeroBlockChannel" ||--|{ "dbo.HeroBlock": "Id"
"dbo.HeroBlockChannel" ||--|{ "dbo.Channel": "Id"
"dbo.UserSection" |o--|{ "dbo.User": "Id"
