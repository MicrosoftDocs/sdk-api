---
UID: NC:clusapi.PCLUSAPI_ADD_CLUSTER_NODE
title: PCLUSAPI_ADD_CLUSTER_NODE
author: windows-sdk-content
description: Adds a node to an existing cluster.
old-location: mscs\addclusternode.htm
old-project: MsCS
ms.assetid: e1d3611e-10d1-4858-923a-01633d2ed78b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_ADD_CLUSTER_NODE, PCLUSAPI_ADD_CLUSTER_NODE callback, PCLUSAPI_ADD_CLUSTER_NODE callback function [Failover Cluster], clusapi/PCLUSAPI_ADD_CLUSTER_NODE, mscs.addclusternode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	UserDefined
 - HeaderDef
: 
api_location:
-	ClusAPI.h
 - accctrl.h
: 
api_name:
-	PCLUSAPI_ADD_CLUSTER_NODE
 - _ACCESS_MODE
: 
product: Windows
targetos: Windows
 - _MULTIPLE_TRUSTEE_OPERATION
: 
 - _PROGRESS_INVOKE_SETTING
: 
 - _SE_OBJECT_TYPE
: 
 - _TRUSTEE_FORM
: 
 - _TRUSTEE_TYPE
: 
req.lib: 
req.dll: 
 - _ACTRL_ACCESS_ENTRYA
: 
 - _ACTRL_ACCESS_ENTRYW
: 
 - _ACTRL_ACCESS_ENTRY_LISTA
: 
 - _ACTRL_ACCESS_ENTRY_LISTW
: 
 - _ACTRL_ALISTA
: 
 - _ACTRL_ALISTW
: 
 - _ACTRL_PROPERTY_ENTRYA
: 
 - _ACTRL_PROPERTY_ENTRYW
: 
 - _EXPLICIT_ACCESS_A
: 
 - _EXPLICIT_ACCESS_W
: 
 - _INHERITED_FROMA
: 
 - _INHERITED_FROMW
: 
 - _OBJECTS_AND_NAME_A
: 
 - _OBJECTS_AND_NAME_W
: 
 - _OBJECTS_AND_SID
: 
 - _TRUSTEE_A
: 
 - _TRUSTEE_W
: 
req.irql: 
 - 
: 
 - BuildExplicitAccessWithNameA
: 
 - BuildExplicitAccessWithNameW
: 
 - BuildSecurityDescriptorA
: 
 - BuildSecurityDescriptorW
: 
 - BuildTrusteeWithNameA
: 
 - BuildTrusteeWithNameW
: 
 - BuildTrusteeWithObjectsAndNameA
: 
 - BuildTrusteeWithObjectsAndNameW
: 
 - BuildTrusteeWithObjectsAndSidA
: 
 - BuildTrusteeWithObjectsAndSidW
: 
 - BuildTrusteeWithSidA
: 
 - BuildTrusteeWithSidW
: 
 - FreeInheritedFromArray
: 
 - GetAuditedPermissionsFromAclA
: 
 - GetAuditedPermissionsFromAclW
: 
 - GetEffectiveRightsFromAclA
: 
 - GetEffectiveRightsFromAclW
: 
 - GetExplicitEntriesFromAclA
: 
 - GetExplicitEntriesFromAclW
: 
 - GetInheritanceSourceA
: 
 - GetInheritanceSourceW
: 
 - GetNamedSecurityInfoA
: 
 - GetNamedSecurityInfoW
: 
 - GetSecurityInfo
: 
 - GetTrusteeFormA
: 
 - GetTrusteeFormW
: 
 - GetTrusteeNameA
: 
 - GetTrusteeNameW
: 
 - GetTrusteeTypeA
: 
 - GetTrusteeTypeW
: 
 - LookupSecurityDescriptorPartsA
: 
 - LookupSecurityDescriptorPartsW
: 
 - SetEntriesInAclA
: 
 - SetEntriesInAclW
: 
 - SetNamedSecurityInfoA
: 
 - SetNamedSecurityInfoW
: 
 - SetSecurityInfo
: 
 - TreeResetNamedSecurityInfoA
: 
 - TreeResetNamedSecurityInfoW
: 
 - TreeSetNamedSecurityInfoA
: 
 - TreeSetNamedSecurityInfoW
: 
 - aclui.h
: 
 - _SI_PAGE_TYPE
: 
 - CreateSecurityPage
: 
 - EditSecurity
: 
 - EditSecurityAdvanced
: 
 - _EFFPERM_RESULT_LIST
: 
 - _SECURITY_OBJECT
: 
 - _SID_INFO
: 
 - _SID_INFO_LIST
: 
 - _SI_ACCESS
: 
 - _SI_INHERIT_TYPE
: 
 - _SI_OBJECT_INFO
: 
 - COM
: 
 - activation.h
: 
 - IActivationFactory.ActivateInstance
: 
 - IActivationFactory
: 
 - activationregistration.h
: 
 - ActivationType
: 
 - IdentityType
: 
 - InstancingType
: 
 - RegistrationScope
: 
 - ThreadingType
: 
 - IActivatableClassRegistration
: 
 - IDllServerActivatableClassRegistration
: 
 - IExeServerActivatableClassRegistration
: 
 - IExeServerRegistration
: 
 - adhoc.h
: 
 - tagDOT11_ADHOC_AUTH_ALGORITHM
: 
 - tagDOT11_ADHOC_CIPHER_ALGORITHM
: 
 - tagDOT11_ADHOC_CONNECT_FAIL_REASON
: 
 - tagDOT11_ADHOC_NETWORK_CONNECTION_STATUS
: 
 - IDot11AdHocInterface.GetActiveNetwork
: 
 - IDot11AdHocInterface.GetDeviceSignature
: 
 - IDot11AdHocInterface.GetFriendlyName
: 
 - IDot11AdHocInterface.GetIEnumDot11AdHocNetworks
: 
 - IDot11AdHocInterface.GetIEnumSecuritySettings
: 
 - IDot11AdHocInterface.GetStatus
: 
 - IDot11AdHocInterface.IsAdHocCapable
: 
 - IDot11AdHocInterface.IsDot11d
: 
 - IDot11AdHocInterface.IsRadioOn
: 
 - IDot11AdHocInterfaceNotificationSink.OnConnectionStatusChange
: 
 - IDot11AdHocManager.CommitCreatedNetwork
: 
 - IDot11AdHocManager.CreateNetwork
: 
 - IDot11AdHocManager.GetIEnumDot11AdHocInterfaces
: 
 - IDot11AdHocManager.GetIEnumDot11AdHocNetworks
: 
 - IDot11AdHocManager.GetNetwork
: 
 - IDot11AdHocManagerNotificationSink.OnInterfaceAdd
: 
 - IDot11AdHocManagerNotificationSink.OnInterfaceRemove
: 
 - IDot11AdHocManagerNotificationSink.OnNetworkAdd
: 
 - IDot11AdHocManagerNotificationSink.OnNetworkRemove
: 
 - IDot11AdHocNetwork.Connect
: 
 - IDot11AdHocNetwork.DeleteProfile
: 
 - IDot11AdHocNetwork.Disconnect
: 
 - IDot11AdHocNetwork.GetContextGuid
: 
 - IDot11AdHocNetwork.GetInterface
: 
 - IDot11AdHocNetwork.GetProfileName
: 
 - IDot11AdHocNetwork.GetSecuritySetting
: 
 - IDot11AdHocNetwork.GetSignalQuality
: 
 - IDot11AdHocNetwork.GetSignature
: 
 - IDot11AdHocNetwork.GetSSID
: 
 - IDot11AdHocNetwork.GetStatus
: 
 - IDot11AdHocNetwork.HasProfile
: 
 - IDot11AdHocNetworkNotificationSink.OnConnectFail
: 
 - IDot11AdHocNetworkNotificationSink.OnStatusChange
: 
 - IDot11AdHocSecuritySettings.GetDot11AuthAlgorithm
: 
 - IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm
: 
 - IEnumDot11AdHocInterfaces.Clone
: 
 - IEnumDot11AdHocInterfaces.Next
: 
 - IEnumDot11AdHocInterfaces.Reset
: 
 - IEnumDot11AdHocInterfaces.Skip
: 
 - IEnumDot11AdHocNetworks.Clone
: 
 - IEnumDot11AdHocNetworks.Next
: 
 - IEnumDot11AdHocNetworks.Reset
: 
 - IEnumDot11AdHocNetworks.Skip
: 
 - IEnumDot11AdHocSecuritySettings.Clone
: 
 - IEnumDot11AdHocSecuritySettings.Next
: 
 - IEnumDot11AdHocSecuritySettings.Reset
: 
 - IEnumDot11AdHocSecuritySettings.Skip
: 
 - IDot11AdHocInterface
: 
 - IDot11AdHocInterfaceNotificationSink
: 
 - IDot11AdHocManager
: 
 - IDot11AdHocManagerNotificationSink
: 
 - IDot11AdHocNetwork
: 
 - IDot11AdHocNetworkNotificationSink
: 
 - IDot11AdHocSecuritySettings
: 
 - IEnumDot11AdHocInterfaces
: 
 - IEnumDot11AdHocNetworks
: 
 - IEnumDot11AdHocSecuritySettings
: 
 - ADsBuildEnumerator
: 
 - ADsBuildVarArrayInt
: 
 - ADsBuildVarArrayStr
: 
 - ADsEncodeBinaryData
: 
 - ADsEnumerateNext
: 
 - ADsFreeEnumerator
: 
 - ADsGetLastError
: 
 - ADsGetObject
: 
 - ADsOpenObject
: 
 - ADsSetLastError
: 
 - AllocADsMem
: 
 - AllocADsStr
: 
 - BinarySDToSecurityDescriptor
: 
 - FreeADsMem
: 
 - FreeADsStr
: 
 - ReallocADsMem
: 
 - ReallocADsStr
: 
 - SecurityDescriptorToBinarySD
: 
 - ADsPropCheckIfWritable
: 
 - ADsPropCreateNotifyObj
: 
 - ADsPropGetInitInfo
: 
 - ADsPropSendErrorMessage
: 
 - ADsPropSetHwnd
: 
 - ADsPropSetHwndWithTitle
: 
 - ADsPropShowErrorDialog
: 
 - adsprop.h
: 
 - _ADSPROPERROR
: 
 - _ADSPROPINITPARAMS
: 
 - adtgen.h
: 
 - _AUDIT_PARAM_TYPE
: 
 - af_irda.h
: 
 - _SOCKADDR_IRDA
: 
 - amaudio.h
: 
 - IAMDirectSound.GetDirectSoundInterface
: 
 - IAMDirectSound.GetFocusWindow
: 
 - IAMDirectSound.GetPrimaryBufferInterface
: 
 - IAMDirectSound.GetSecondaryBufferInterface
: 
 - IAMDirectSound.ReleaseDirectSoundInterface
: 
 - IAMDirectSound.ReleasePrimaryBufferInterface
: 
 - IAMDirectSound.ReleaseSecondaryBufferInterface
: 
 - IAMDirectSound.SetFocusWindow
: 
 - IAMDirectSound
: 
 - amparse.h
: 
 - IAMParse.Flush
: 
 - IAMParse.GetParseTime
: 
 - IAMParse.SetParseTime
: 
 - IAMParse
: 
 - amsi.h
: 
 - AMSI_ATTRIBUTE
: 
 - AMSI_RESULT
: 
 - AmsiCloseSession
: 
 - AmsiInitialize
: 
 - AmsiOpenSession
: 
 - AmsiResultIsMalware
: 
 - AmsiScanBuffer
: 
 - AmsiScanString
: 
 - AmsiUninitialize
: 
 - IAmsiStream.GetAttribute
: 
 - IAmsiStream.Read
: 
 - IAntimalware.Scan
: 
 - IAntimalwareProvider.DisplayName
: 
 - IAntimalwareProvider.Scan
: 
 - IAmsiStream
: 
 - IAntimalware
: 
 - IAntimalwareProvider
: 
 - amstream.h
: 
 - IAMMediaStream.Initialize
: 
 - IAMMediaStream.JoinAMMultiMediaStream
: 
 - IAMMediaStream.JoinFilter
: 
 - IAMMediaStream.JoinFilterGraph
: 
 - IAMMediaStream.SetState
: 
 - IAMMediaTypeSample.GetActualDataLength
: 
 - IAMMediaTypeSample.GetMediaTime
: 
 - IAMMediaTypeSample.GetMediaType
: 
 - IAMMediaTypeSample.GetPointer
: 
 - IAMMediaTypeSample.GetSize
: 
 - IAMMediaTypeSample.GetTime
: 
 - IAMMediaTypeSample.IsDiscontinuity
: 
 - IAMMediaTypeSample.IsPreroll
: 
 - IAMMediaTypeSample.IsSyncPoint
: 
 - IAMMediaTypeSample.SetActualDataLength
: 
 - IAMMediaTypeSample.SetDiscontinuity
: 
 - IAMMediaTypeSample.SetMediaTime
: 
 - IAMMediaTypeSample.SetMediaType
: 
 - IAMMediaTypeSample.SetPointer
: 
 - IAMMediaTypeSample.SetPreroll
: 
 - IAMMediaTypeSample.SetSyncPoint
: 
 - IAMMediaTypeSample.SetTime
: 
 - IAMMediaTypeStream.CreateSample
: 
 - IAMMediaTypeStream.GetFormat
: 
 - IAMMediaTypeStream.GetStreamAllocatorRequirements
: 
 - IAMMediaTypeStream.SetFormat
: 
 - IAMMediaTypeStream.SetStreamAllocatorRequirements
: 
 - IAMMultiMediaStream.AddMediaStream
: 
 - IAMMultiMediaStream.GetFilter
: 
 - IAMMultiMediaStream.GetFilterGraph
: 
 - IAMMultiMediaStream.Initialize
: 
 - IAMMultiMediaStream.OpenFile
: 
 - IAMMultiMediaStream.OpenMoniker
: 
 - IAMMultiMediaStream.Render
: 
 - IDirectDrawMediaSample.GetSurfaceAndReleaseLock
: 
 - IDirectDrawMediaSample.LockMediaSamplePointer
: 
 - IDirectDrawMediaSampleAllocator.GetDirectDraw
: 
 - IMediaStreamFilter.AddMediaStream
: 
 - IMediaStreamFilter.EndOfStream
: 
 - IMediaStreamFilter.EnumMediaStreams
: 
 - IMediaStreamFilter.Flush
: 
 - IMediaStreamFilter.GetCurrentStreamTime
: 
 - IMediaStreamFilter.GetMediaStream
: 
 - IMediaStreamFilter.ReferenceTimeToStreamTime
: 
 - IMediaStreamFilter.SupportSeeking
: 
 - IMediaStreamFilter.WaitUntil
: 
 - IAMMediaStream
: 
 - IAMMediaTypeSample
: 
 - IAMMediaTypeStream
: 
 - IAMMultiMediaStream
: 
 - IDirectDrawMediaSample
: 
 - IDirectDrawMediaSampleAllocator
: 
 - IMediaStreamFilter
: 
 - amva.h
: 
 - _tag_AMVABeginFrameInfo
: 
 - _tag_AMVABUFFERINFO
: 
 - _tag_AMVACompBufferInfo
: 
 - _tag_AMVAEndFrameInfo
: 
 - _tag_AMVAInternalMemInfo
: 
 - _tag_AMVAUncompBufferInfo
: 
 - _tag_AMVAUncompDataInfo
: 
 - amvideo.h
: 
 - BITMASKS
: 
 - BIT_MASKS_MATCH
: 
 - COLORS
: 
 - DIBSIZE
: 
 - HEADER
: 
 - IDirectDrawVideo.CanUseOverlayStretch
: 
 - IDirectDrawVideo.CanUseScanLine
: 
 - IDirectDrawVideo.GetCaps
: 
 - IDirectDrawVideo.GetDirectDraw
: 
 - IDirectDrawVideo.GetEmulatedCaps
: 
 - IDirectDrawVideo.GetFourCCCodes
: 
 - IDirectDrawVideo.GetSurfaceDesc
: 
 - IDirectDrawVideo.GetSurfaceType
: 
 - IDirectDrawVideo.GetSwitches
: 
 - IDirectDrawVideo.SetDefault
: 
 - IDirectDrawVideo.SetDirectDraw
: 
 - IDirectDrawVideo.SetSwitches
: 
 - IDirectDrawVideo.UseOverlayStretch
: 
 - IDirectDrawVideo.UseScanLine
: 
 - IDirectDrawVideo.UseWhenFullScreen
: 
 - IDirectDrawVideo.WillUseFullScreen
: 
 - IFullScreenVideoEx.CountModes
: 
 - IFullScreenVideoEx.GetAcceleratorTable
: 
 - IFullScreenVideoEx.GetCaption
: 
 - IFullScreenVideoEx.GetClipFactor
: 
 - IFullScreenVideoEx.GetCurrentMode
: 
 - IFullScreenVideoEx.GetMessageDrain
: 
 - IFullScreenVideoEx.GetModeInfo
: 
 - IFullScreenVideoEx.GetMonitor
: 
 - IFullScreenVideoEx.HideOnDeactivate
: 
 - IFullScreenVideoEx.IsHideOnDeactivate
: 
 - IFullScreenVideoEx.IsKeepPixelAspectRatio
: 
 - IFullScreenVideoEx.IsModeAvailable
: 
 - IFullScreenVideoEx.IsModeEnabled
: 
 - IFullScreenVideoEx.KeepPixelAspectRatio
: 
 - IFullScreenVideoEx.SetAcceleratorTable
: 
 - IFullScreenVideoEx.SetCaption
: 
 - IFullScreenVideoEx.SetClipFactor
: 
 - IFullScreenVideoEx.SetDefault
: 
 - IFullScreenVideoEx.SetEnabled
: 
 - IFullScreenVideoEx.SetMessageDrain
: 
 - IFullScreenVideoEx.SetMonitor
: 
 - IQualProp.get_AvgFrameRate
: 
 - IQualProp.get_AvgSyncOffset
: 
 - IQualProp.get_DevSyncOffset
: 
 - IQualProp.get_FramesDrawn
: 
 - IQualProp.get_FramesDroppedInRenderer
: 
 - IQualProp.get_Jitter
: 
 - MPEG1_SEQUENCE_INFO
: 
 - PALETTE_ENTRIES
: 
 - PALETTISED
: 
 - RESET_HEADER
: 
 - RESET_MASKS
: 
 - RESET_PALETTE
: 
 - SIZE_MPEG1VIDEOINFO
: 
 - IDirectDrawVideo
: 
 - IFullScreenVideoEx
: 
 - IQualProp
: 
 - tagAnalogVideoInfo
: 
 - tagMPEG1VIDEOINFO
: 
 - tagVIDEOINFO
: 
 - tagVIDEOINFOHEADER
: 
 - tag_TRUECOLORINFO
: 
 - _AM_FRAMESTEP_STEP
: 
 - amxmlgraphbuilder.h
: 
 - IXMLGraphBuilder.BuildFromXML
: 
 - IXMLGraphBuilder.BuildFromXMLFile
: 
 - IXMLGraphBuilder.SaveToXML
: 
 - IXMLGraphBuilder
: 
 - ApphelpCheckShellObject
: 
 - appmgmt.h
: 
 - _INSTALLSPECTYPE
: 
 - GetLocalManagedApplications
: 
 - GetManagedApplicationCategories
: 
 - GetManagedApplications
: 
 - InstallApplication
: 
 - UninstallApplication
: 
 - _APPCATEGORYINFO
: 
 - _APPCATEGORYINFOLIST
: 
 - _INSTALLDATA
: 
 - _INSTALLSPEC
: 
 - _LOCALMANAGEDAPPLICATION
: 
 - _MANAGEDAPPLICATION
: 
 - appmodel.h
: 
 - PackageOrigin
: 
 - ClosePackageInfo
: 
 - FindPackagesByPackageFamily
: 
 - FormatApplicationUserModelId
: 
 - GetApplicationUserModelId
: 
 - GetApplicationUserModelIdFromToken
: 
 - GetCurrentApplicationUserModelId
: 
 - GetCurrentPackageFamilyName
: 
 - GetCurrentPackageFullName
: 
 - GetCurrentPackageId
: 
 - GetCurrentPackageInfo
: 
 - GetCurrentPackagePath
: 
 - GetPackageApplicationIds
: 
 - GetPackageFamilyName
: 
 - GetPackageFamilyNameFromToken
: 
 - GetPackageFullName
: 
 - GetPackageFullNameFromToken
: 
 - GetPackageId
: 
 - GetPackageInfo
: 
 - GetPackagePath
: 
 - GetPackagePathByFullName
: 
 - GetPackagesByPackageFamily
: 
 - GetStagedPackageOrigin
: 
 - GetStagedPackagePathByFullName
: 
 - OpenPackageInfoByFullName
: 
 - PackageFamilyNameFromFullName
: 
 - PackageFamilyNameFromId
: 
 - PackageFullNameFromId
: 
 - PackageIdFromFullName
: 
 - PackageNameAndPublisherIdFromFamilyName
: 
 - ParseApplicationUserModelId
: 
 - PACKAGE_ID
: 
 - PACKAGE_INFO
: 
 - PACKAGE_VERSION
: 
 - UserDefined
: 
 - appnotify.h
: 
 - PAPPSTATE_CHANGE_ROUTINE
: 
 - RegisterAppStateChangeNotification
: 
 - UnregisterAppStateChangeNotification
: 
 - appxpackaging.h
: 
 - APPX_BUNDLE_FOOTPRINT_FILE_TYPE
: 
 - APPX_BUNDLE_PAYLOAD_PACKAGE_TYPE
: 
 - APPX_CAPABILITIES
: 
 - APPX_COMPRESSION_OPTION
: 
 - APPX_ENCRYPTED_PACKAGE_OPTIONS
: 
 - APPX_FOOTPRINT_FILE_TYPE
: 
 - APPX_PACKAGE_ARCHITECTURE
: 
 - APPX_PACKAGE_ARCHITECTURE2
: 
 - APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_MANIFEST_OPTIONS
: 
 - APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
: 
 - IAppxBlockMapBlock.GetCompressedSize
: 
 - IAppxBlockMapBlock.GetHash
: 
 - IAppxBlockMapBlocksEnumerator.GetCurrent
: 
 - IAppxBlockMapBlocksEnumerator.GetHasCurrent
: 
 - IAppxBlockMapBlocksEnumerator.MoveNext
: 
 - IAppxBlockMapFile.GetBlocks
: 
 - IAppxBlockMapFile.GetLocalFileHeaderSize
: 
 - IAppxBlockMapFile.GetName
: 
 - IAppxBlockMapFile.GetUncompressedSize
: 
 - IAppxBlockMapFile.ValidateFileHash
: 
 - IAppxBlockMapFilesEnumerator.GetCurrent
: 
 - IAppxBlockMapFilesEnumerator.GetHasCurrent
: 
 - IAppxBlockMapFilesEnumerator.MoveNext
: 
 - IAppxBlockMapReader.GetFile
: 
 - IAppxBlockMapReader.GetFiles
: 
 - IAppxBlockMapReader.GetHashMethod
: 
 - IAppxBlockMapReader.GetStream
: 
 - IAppxBundleFactory.CreateBundleManifestReader
: 
 - IAppxBundleFactory.CreateBundleReader
: 
 - IAppxBundleFactory.CreateBundleWriter
: 
 - IAppxBundleManifestOptionalBundleInfo.GetFileName
: 
 - IAppxBundleManifestOptionalBundleInfo.GetPackageId
: 
 - IAppxBundleManifestOptionalBundleInfo.GetPackageInfoItems
: 
 - IAppxBundleManifestOptionalBundleInfoEnumerator.GetCurrent
: 
 - IAppxBundleManifestOptionalBundleInfoEnumerator.GetHasCurrent
: 
 - IAppxBundleManifestOptionalBundleInfoEnumerator.MoveNext
: 
 - IAppxBundleManifestPackageInfo.GetFileName
: 
 - IAppxBundleManifestPackageInfo.GetOffset
: 
 - IAppxBundleManifestPackageInfo.GetPackageId
: 
 - IAppxBundleManifestPackageInfo.GetPackageType
: 
 - IAppxBundleManifestPackageInfo.GetResources
: 
 - IAppxBundleManifestPackageInfo.GetSize
: 
 - IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage
: 
 - IAppxBundleManifestPackageInfo2.GetIsNonQualifiedResourcePackage
: 
 - IAppxBundleManifestPackageInfo2.GetIsPackageReference
: 
 - IAppxBundleManifestPackageInfoEnumerator.GetCurrent
: 
 - IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent
: 
 - IAppxBundleManifestPackageInfoEnumerator.MoveNext
: 
 - IAppxBundleManifestReader.GetPackageId
: 
 - IAppxBundleManifestReader.GetPackageInfoItems
: 
 - IAppxBundleManifestReader.GetStream
: 
 - IAppxBundleManifestReader2.GetOptionalBundles
: 
 - IAppxBundleReader.GetBlockMap
: 
 - IAppxBundleReader.GetFootprintFile
: 
 - IAppxBundleReader.GetManifest
: 
 - IAppxBundleReader.GetPayloadPackage
: 
 - IAppxBundleReader.GetPayloadPackages
: 
 - IAppxBundleWriter.AddPayloadPackage
: 
 - IAppxBundleWriter.Close
: 
 - IAppxBundleWriter2.AddExternalPackageReference
: 
 - IAppxBundleWriter3.AddPackageReference
: 
 - IAppxBundleWriter3.Close
: 
 - IAppxBundleWriter4.AddExternalPackageReference
: 
 - IAppxBundleWriter4.AddPackageReference
: 
 - IAppxBundleWriter4.AddPayloadPackage
: 
 - IAppxContentGroup.GetFiles
: 
 - IAppxContentGroup.GetName
: 
 - IAppxContentGroupFilesEnumerator.GetCurrent
: 
 - IAppxContentGroupFilesEnumerator.GetHasCurrent
: 
 - IAppxContentGroupFilesEnumerator.MoveNext
: 
 - IAppxContentGroupMapReader.GetAutomaticGroups
: 
 - IAppxContentGroupMapReader.GetRequiredGroup
: 
 - IAppxContentGroupMapWriter.AddAutomaticFile
: 
 - IAppxContentGroupMapWriter.AddAutomaticGroup
: 
 - IAppxContentGroupsEnumerator.GetCurrent
: 
 - IAppxContentGroupsEnumerator.GetHasCurrent
: 
 - IAppxContentGroupsEnumerator.MoveNext
: 
 - IAppxEncryptedBundleWriter.AddPayloadPackageEncrypted
: 
 - IAppxEncryptedBundleWriter.Close
: 
 - IAppxEncryptedBundleWriter2.AddExternalPackageReference
: 
 - IAppxEncryptedBundleWriter3.AddExternalPackageReference
: 
 - IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted
: 
 - IAppxEncryptedPackageWriter.AddPayloadFileEncrypted
: 
 - IAppxEncryptedPackageWriter.Close
: 
 - IAppxEncryptedPackageWriter2.AddPayloadFilesEncrypted
: 
 - IAppxEncryptionFactory.CreateEncryptedBundleReader
: 
 - IAppxEncryptionFactory.CreateEncryptedBundleWriter
: 
 - IAppxEncryptionFactory.CreateEncryptedPackageReader
: 
 - IAppxEncryptionFactory.CreateEncryptedPackageWriter
: 
 - IAppxEncryptionFactory.DecryptBundle
: 
 - IAppxEncryptionFactory.DecryptPackage
: 
 - IAppxEncryptionFactory.EncryptBundle
: 
 - IAppxEncryptionFactory.EncryptPackage
: 
 - IAppxEncryptionFactory2.CreateEncryptedPackageWriter
: 
 - IAppxEncryptionFactory3.CreateEncryptedBundleWriter
: 
 - IAppxEncryptionFactory3.CreateEncryptedPackageWriter
: 
 - IAppxEncryptionFactory3.EncryptBundle
: 
 - IAppxEncryptionFactory3.EncryptPackage
: 
 - IAppxEncryptionFactory4.EncryptPackage
: 
 - IAppxFactory.CreateBlockMapReader
: 
 - IAppxFactory.CreateManifestReader
: 
 - IAppxFactory.CreatePackageReader
: 
 - IAppxFactory.CreatePackageWriter
: 
 - IAppxFactory.CreateValidatedBlockMapReader
: 
 - IAppxFactory2.CreateContentGroupMapReader
: 
 - IAppxFactory2.CreateContentGroupMapWriter
: 
 - IAppxFactory2.CreateSourceContentGroupMapReader
: 
 - IAppxFile.GetCompressionOption
: 
 - IAppxFile.GetContentType
: 
 - IAppxFile.GetName
: 
 - IAppxFile.GetSize
: 
 - IAppxFile.GetStream
: 
 - IAppxFilesEnumerator.GetCurrent
: 
 - IAppxFilesEnumerator.GetHasCurrent
: 
 - IAppxFilesEnumerator.MoveNext
: 
 - IAppxManifestApplication.GetAppUserModelId
: 
 - IAppxManifestApplication.GetStringValue
: 
 - IAppxManifestApplicationsEnumerator.GetCurrent
: 
 - IAppxManifestApplicationsEnumerator.GetHasCurrent
: 
 - IAppxManifestApplicationsEnumerator.MoveNext
: 
 - IAppxManifestDeviceCapabilitiesEnumerator.GetCurrent
: 
 - IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent
: 
 - IAppxManifestDeviceCapabilitiesEnumerator.MoveNext
: 
 - IAppxManifestMainPackageDependenciesEnumerator.GetCurrent
: 
 - IAppxManifestMainPackageDependenciesEnumerator.GetHasCurrent
: 
 - IAppxManifestMainPackageDependenciesEnumerator.MoveNext
: 
 - IAppxManifestMainPackageDependency.GetName
: 
 - IAppxManifestMainPackageDependency.GetPackageFamilyName
: 
 - IAppxManifestMainPackageDependency.GetPublisher
: 
 - IAppxManifestOptionalPackageInfo.GetIsOptionalPackage
: 
 - IAppxManifestOptionalPackageInfo.GetMainPackageName
: 
 - IAppxManifestPackageDependenciesEnumerator.GetCurrent
: 
 - IAppxManifestPackageDependenciesEnumerator.GetHasCurrent
: 
 - IAppxManifestPackageDependenciesEnumerator.MoveNext
: 
 - IAppxManifestPackageDependency.GetMinVersion
: 
 - IAppxManifestPackageDependency.GetName
: 
 - IAppxManifestPackageDependency.GetPublisher
: 
 - IAppxManifestPackageDependency2.GetMaxMajorVersionTested
: 
 - IAppxManifestPackageId.ComparePublisher
: 
 - IAppxManifestPackageId.GetArchitecture
: 
 - IAppxManifestPackageId.GetName
: 
 - IAppxManifestPackageId.GetPackageFamilyName
: 
 - IAppxManifestPackageId.GetPackageFullName
: 
 - IAppxManifestPackageId.GetPublisher
: 
 - IAppxManifestPackageId.GetResourceId
: 
 - IAppxManifestPackageId.GetVersion
: 
 - IAppxManifestProperties.GetBoolValue
: 
 - IAppxManifestProperties.GetStringValue
: 
 - IAppxManifestReader.GetApplications
: 
 - IAppxManifestReader.GetCapabilities
: 
 - IAppxManifestReader.GetDeviceCapabilities
: 
 - IAppxManifestReader.GetPackageDependencies
: 
 - IAppxManifestReader.GetPackageId
: 
 - IAppxManifestReader.GetPrerequisite
: 
 - IAppxManifestReader.GetProperties
: 
 - IAppxManifestReader.GetResources
: 
 - IAppxManifestReader.GetStream
: 
 - IAppxManifestReader2.GetQualifiedResources
: 
 - IAppxManifestReader5.GetMainPackageDependencies
: 
 - IAppxManifestReader6.GetIsNonQualifiedResourcePackage
: 
 - IAppxManifestResourcesEnumerator.GetCurrent
: 
 - IAppxManifestResourcesEnumerator.GetHasCurrent
: 
 - IAppxManifestResourcesEnumerator.MoveNext
: 
 - IAppxManifestTargetDeviceFamily.GetMaxVersionTested
: 
 - IAppxManifestTargetDeviceFamily.GetMinVersion
: 
 - IAppxManifestTargetDeviceFamily.GetName
: 
 - IAppxPackageEditor.CreateDeltaPackage
: 
 - IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap
: 
 - IAppxPackageEditor.UpdateEncryptedPackage
: 
 - IAppxPackageEditor.UpdatePackage
: 
 - IAppxPackageEditor.UpdatePackageManifest
: 
 - IAppxPackageReader.GetBlockMap
: 
 - IAppxPackageReader.GetFootprintFile
: 
 - IAppxPackageReader.GetManifest
: 
 - IAppxPackageReader.GetPayloadFile
: 
 - IAppxPackageReader.GetPayloadFiles
: 
 - IAppxPackageReader2.GetContentGroupMap
: 
 - IAppxPackageWriter.AddPayloadFile
: 
 - IAppxPackageWriter.Close
: 
 - IAppxPackageWriter2.Close
: 
 - IAppxPackageWriter3.AddPayloadFiles
: 
 - IAppxSourceContentGroupMapReader.GetAutomaticGroups
: 
 - IAppxSourceContentGroupMapReader.GetRequiredGroup
: 
 - IAppxBlockMapBlock
: 
 - IAppxBlockMapBlocksEnumerator
: 
 - IAppxBlockMapFile
: 
 - IAppxBlockMapFilesEnumerator
: 
 - IAppxBlockMapReader
: 
 - IAppxBundleFactory
: 
 - IAppxBundleManifestOptionalBundleInfo
: 
 - IAppxBundleManifestOptionalBundleInfoEnumerator
: 
 - IAppxBundleManifestPackageInfo
: 
 - IAppxBundleManifestPackageInfo2
: 
 - IAppxBundleManifestPackageInfoEnumerator
: 
 - IAppxBundleManifestReader
: 
 - IAppxBundleManifestReader2
: 
 - IAppxBundleReader
: 
 - IAppxBundleWriter
: 
 - IAppxBundleWriter2
: 
 - IAppxBundleWriter3
: 
 - IAppxBundleWriter4
: 
 - IAppxContentGroup
: 
 - IAppxContentGroupFilesEnumerator
: 
 - IAppxContentGroupMapReader
: 
 - IAppxContentGroupMapWriter
: 
 - IAppxContentGroupsEnumerator
: 
 - IAppxEncryptedBundleWriter
: 
 - IAppxEncryptedBundleWriter2
: 
 - IAppxEncryptedBundleWriter3
: 
 - IAppxEncryptedPackageWriter
: 
 - IAppxEncryptedPackageWriter2
: 
 - IAppxEncryptionFactory
: 
 - IAppxEncryptionFactory2
: 
 - IAppxEncryptionFactory3
: 
 - IAppxEncryptionFactory4
: 
 - IAppxFactory
: 
 - IAppxFactory2
: 
 - IAppxFile
: 
 - IAppxFilesEnumerator
: 
 - IAppxManifestApplication
: 
 - IAppxManifestApplicationsEnumerator
: 
 - IAppxManifestDeviceCapabilitiesEnumerator
: 
 - IAppxManifestMainPackageDependenciesEnumerator
: 
 - IAppxManifestMainPackageDependency
: 
 - IAppxManifestOptionalPackageInfo
: 
 - IAppxManifestPackageDependenciesEnumerator
: 
 - IAppxManifestPackageDependency
: 
 - IAppxManifestPackageDependency2
: 
 - IAppxManifestPackageId
: 
 - IAppxManifestPackageId2
: 
 - IAppxManifestProperties
: 
 - IAppxManifestReader
: 
 - IAppxManifestReader2
: 
 - IAppxManifestReader5
: 
 - IAppxManifestReader6
: 
 - IAppxManifestResourcesEnumerator
: 
 - IAppxManifestTargetDeviceFamily
: 
 - IAppxPackageEditor
: 
 - IAppxPackageReader
: 
 - IAppxPackageReader2
: 
 - IAppxPackageWriter
: 
 - IAppxPackageWriter2
: 
 - IAppxPackageWriter3
: 
 - IAppxSourceContentGroupMapReader
: 
 - APPX_ENCRYPTED_EXEMPTIONS
: 
 - APPX_ENCRYPTED_PACKAGE_SETTINGS
: 
 - APPX_ENCRYPTED_PACKAGE_SETTINGS2
: 
 - APPX_KEY_INFO
: 
 - APPX_PACKAGE_SETTINGS
: 
 - APPX_PACKAGE_WRITER_PAYLOAD_STREAM
: 
 - asyncinfo.h
: 
 - AsyncStatus
: 
 - IAsyncInfo.Cancel
: 
 - IAsyncInfo.Close
: 
 - IAsyncInfo.get_ErrorCode
: 
 - IAsyncInfo.get_Id
: 
 - IAsyncInfo.get_Status
: 
 - IAsyncInfo
: 
 - GetNetScheduleAccountInformation
: 
 - SetNetScheduleAccountInformation
: 
 - AtlThunk_AllocateData
: 
 - AtlThunk_DataToCode
: 
 - AtlThunk_FreeData
: 
 - AtlThunk_InitData
: 
 - atscpsipparser.h
: 
 - IAtscContentAdvisoryDescriptor.GetLength
: 
 - IAtscContentAdvisoryDescriptor.GetRatingRegionCount
: 
 - IAtscContentAdvisoryDescriptor.GetRecordRatedDimensions
: 
 - IAtscContentAdvisoryDescriptor.GetRecordRatingDescriptionText
: 
 - IAtscContentAdvisoryDescriptor.GetRecordRatingDimension
: 
 - IAtscContentAdvisoryDescriptor.GetRecordRatingRegion
: 
 - IAtscContentAdvisoryDescriptor.GetRecordRatingValue
: 
 - IAtscContentAdvisoryDescriptor.GetTag
: 
 - IAtscPsipParser.GetCAT
: 
 - IAtscPsipParser.GetEAS
: 
 - IAtscPsipParser.GetEIT
: 
 - IAtscPsipParser.GetETT
: 
 - IAtscPsipParser.GetMGT
: 
 - IAtscPsipParser.GetPAT
: 
 - IAtscPsipParser.GetPMT
: 
 - IAtscPsipParser.GetSTT
: 
 - IAtscPsipParser.GetTSDT
: 
 - IAtscPsipParser.GetVCT
: 
 - IAtscPsipParser.Initialize
: 
 - IATSC_EIT.GetCountOfRecords
: 
 - IATSC_EIT.GetProtocolVersion
: 
 - IATSC_EIT.GetRecordCountOfDescriptors
: 
 - IATSC_EIT.GetRecordDescriptorByIndex
: 
 - IATSC_EIT.GetRecordDescriptorByTag
: 
 - IATSC_EIT.GetRecordDuration
: 
 - IATSC_EIT.GetRecordEtmLocation
: 
 - IATSC_EIT.GetRecordEventId
: 
 - IATSC_EIT.GetRecordStartTime
: 
 - IATSC_EIT.GetRecordTitleText
: 
 - IATSC_EIT.GetSourceId
: 
 - IATSC_EIT.GetVersionNumber
: 
 - IATSC_EIT.Initialize
: 
 - IATSC_ETT.GetEtmId
: 
 - IATSC_ETT.GetExtendedMessageText
: 
 - IATSC_ETT.GetProtocolVersion
: 
 - IATSC_ETT.GetVersionNumber
: 
 - IATSC_ETT.Initialize
: 
 - IATSC_MGT.GetCountOfRecords
: 
 - IATSC_MGT.GetCountOfTableDescriptors
: 
 - IATSC_MGT.GetProtocolVersion
: 
 - IATSC_MGT.GetRecordCountOfDescriptors
: 
 - IATSC_MGT.GetRecordDescriptorByIndex
: 
 - IATSC_MGT.GetRecordDescriptorByTag
: 
 - IATSC_MGT.GetRecordType
: 
 - IATSC_MGT.GetRecordTypePid
: 
 - IATSC_MGT.GetRecordVersionNumber
: 
 - IATSC_MGT.GetTableDescriptorByIndex
: 
 - IATSC_MGT.GetTableDescriptorByTag
: 
 - IATSC_MGT.GetVersionNumber
: 
 - IATSC_MGT.Initialize
: 
 - IATSC_STT.GetCountOfTableDescriptors
: 
 - IATSC_STT.GetDaylightSavings
: 
 - IATSC_STT.GetGpsUtcOffset
: 
 - IATSC_STT.GetProtocolVersion
: 
 - IATSC_STT.GetSystemTime
: 
 - IATSC_STT.GetTableDescriptorByIndex
: 
 - IATSC_STT.GetTableDescriptorByTag
: 
 - IATSC_STT.Initialize
: 
 - IATSC_VCT.GetCountOfRecords
: 
 - IATSC_VCT.GetCountOfTableDescriptors
: 
 - IATSC_VCT.GetProtocolVersion
: 
 - IATSC_VCT.GetRecordCarrierFrequency
: 
 - IATSC_VCT.GetRecordCountOfDescriptors
: 
 - IATSC_VCT.GetRecordDescriptorByIndex
: 
 - IATSC_VCT.GetRecordDescriptorByTag
: 
 - IATSC_VCT.GetRecordEtmLocation
: 
 - IATSC_VCT.GetRecordIsAccessControlledBitSet
: 
 - IATSC_VCT.GetRecordIsHiddenBitSet
: 
 - IATSC_VCT.GetRecordIsHideGuideBitSet
: 
 - IATSC_VCT.GetRecordIsOutOfBandBitSet
: 
 - IATSC_VCT.GetRecordIsPathSelectBitSet
: 
 - IATSC_VCT.GetRecordMajorChannelNumber
: 
 - IATSC_VCT.GetRecordMinorChannelNumber
: 
 - IATSC_VCT.GetRecordModulationMode
: 
 - IATSC_VCT.GetRecordName
: 
 - IATSC_VCT.GetRecordProgramNumber
: 
 - IATSC_VCT.GetRecordServiceType
: 
 - IATSC_VCT.GetRecordSourceId
: 
 - IATSC_VCT.GetRecordTransportStreamId
: 
 - IATSC_VCT.GetTableDescriptorByIndex
: 
 - IATSC_VCT.GetTableDescriptorByTag
: 
 - IATSC_VCT.GetTransportStreamId
: 
 - IATSC_VCT.GetVersionNumber
: 
 - IATSC_VCT.Initialize
: 
 - ICaptionServiceDescriptor.GetCaptionServiceNumber
: 
 - ICaptionServiceDescriptor.GetCCType
: 
 - ICaptionServiceDescriptor.GetEasyReader
: 
 - ICaptionServiceDescriptor.GetLanguageCode
: 
 - ICaptionServiceDescriptor.GetNumberOfServices
: 
 - ICaptionServiceDescriptor.GetWideAspectRatio
: 
 - ISCTE_EAS.GetAlertPriority
: 
 - ISCTE_EAS.GetAlertText
: 
 - ISCTE_EAS.GetCountOfTableDescriptors
: 
 - ISCTE_EAS.GetDetailsAudioOOBSourceID
: 
 - ISCTE_EAS.GetDetailsMajor
: 
 - ISCTE_EAS.GetDetailsMinor
: 
 - ISCTE_EAS.GetDetailsOOBSourceID
: 
 - ISCTE_EAS.GetDuration
: 
 - ISCTE_EAS.GetEASEventCode
: 
 - ISCTE_EAS.GetEASEventCodeLen
: 
 - ISCTE_EAS.GetEASEventID
: 
 - ISCTE_EAS.GetExceptionCount
: 
 - ISCTE_EAS.GetExceptionService
: 
 - ISCTE_EAS.GetLocationCodes
: 
 - ISCTE_EAS.GetLocationCount
: 
 - ISCTE_EAS.GetNatureOfActivationText
: 
 - ISCTE_EAS.GetOriginatorCode
: 
 - ISCTE_EAS.GetProtocolVersion
: 
 - ISCTE_EAS.GetRawAlertText
: 
 - ISCTE_EAS.GetRawAlertTextLen
: 
 - ISCTE_EAS.GetRawNatureOfActivationText
: 
 - ISCTE_EAS.GetRawNatureOfActivationTextLen
: 
 - ISCTE_EAS.GetSequencyNumber
: 
 - ISCTE_EAS.GetStartTime
: 
 - ISCTE_EAS.GetTableDescriptorByIndex
: 
 - ISCTE_EAS.GetTableDescriptorByTag
: 
 - ISCTE_EAS.GetTimeRemaining
: 
 - ISCTE_EAS.GetVersionNumber
: 
 - ISCTE_EAS.Initialize
: 
 - IServiceLocationDescriptor.GetElementLanguageCode
: 
 - IServiceLocationDescriptor.GetElementPID
: 
 - IServiceLocationDescriptor.GetElementStreamType
: 
 - IServiceLocationDescriptor.GetNumberOfElements
: 
 - IServiceLocationDescriptor.GetPCR_PID
: 
 - IAtscContentAdvisoryDescriptor
: 
 - IAtscPsipParser
: 
 - IATSC_EIT
: 
 - IATSC_ETT
: 
 - IATSC_MGT
: 
 - IATSC_STT
: 
 - IATSC_VCT
: 
 - ICaptionServiceDescriptor
: 
 - ISCTE_EAS
: 
 - IServiceLocationDescriptor
: 
 - audevcod.h
: 
 - _tagSND_DEVICE_ERROR
: 
 - audioapotypes.h
: 
 - APO_BUFFER_FLAGS
: 
 - APO_CONNECTION_PROPERTY
: 
 - audioclient.h
: 
 - AUDCLNT_STREAMOPTIONS
: 
 - _AUDCLNT_BUFFERFLAGS
: 
 - IAudioCaptureClient.GetBuffer
: 
 - IAudioCaptureClient.GetNextPacketSize
: 
 - IAudioCaptureClient.ReleaseBuffer
: 
 - IAudioClient.GetBufferSize
: 
 - IAudioClient.GetCurrentPadding
: 
 - IAudioClient.GetDevicePeriod
: 
 - IAudioClient.GetMixFormat
: 
 - IAudioClient.GetService
: 
 - IAudioClient.GetStreamLatency
: 
 - IAudioClient.Initialize
: 
 - IAudioClient.IsFormatSupported
: 
 - IAudioClient.Reset
: 
 - IAudioClient.SetEventHandle
: 
 - IAudioClient.Start
: 
 - IAudioClient.Stop
: 
 - IAudioClient2.GetBufferSizeLimits
: 
 - IAudioClient2.IsOffloadCapable
: 
 - IAudioClient2.SetClientProperties
: 
 - IAudioClient3.GetCurrentSharedModeEnginePeriod
: 
 - IAudioClient3.GetSharedModeEnginePeriod
: 
 - IAudioClient3.InitializeSharedAudioStream
: 
 - IAudioClock.GetCharacteristics
: 
 - IAudioClock.GetFrequency
: 
 - IAudioClock.GetPosition
: 
 - IAudioClock2.GetDevicePosition
: 
 - IAudioClockAdjustment.SetSampleRate
: 
 - IAudioRenderClient.GetBuffer
: 
 - IAudioRenderClient.ReleaseBuffer
: 
 - IAudioStreamVolume.GetAllVolumes
: 
 - IAudioStreamVolume.GetChannelCount
: 
 - IAudioStreamVolume.GetChannelVolume
: 
 - IAudioStreamVolume.SetAllVolumes
: 
 - IAudioStreamVolume.SetChannelVolume
: 
 - IChannelAudioVolume.GetAllVolumes
: 
 - IChannelAudioVolume.GetChannelCount
: 
 - IChannelAudioVolume.GetChannelVolume
: 
 - IChannelAudioVolume.SetAllVolumes
: 
 - IChannelAudioVolume.SetChannelVolume
: 
 - ISimpleAudioVolume.GetMasterVolume
: 
 - ISimpleAudioVolume.GetMute
: 
 - ISimpleAudioVolume.SetMasterVolume
: 
 - ISimpleAudioVolume.SetMute
: 
 - IAudioCaptureClient
: 
 - IAudioClient
: 
 - IAudioClient2
: 
 - IAudioClient3
: 
 - IAudioClock
: 
 - IAudioClock2
: 
 - IAudioClockAdjustment
: 
 - IAudioRenderClient
: 
 - IAudioStreamVolume
: 
 - IChannelAudioVolume
: 
 - ISimpleAudioVolume
: 
 - AudioClientProperties
: 
 - audioendpoints.h
: 
 - IAudioEndpointFormatControl.ResetToDefault
: 
 - IAudioEndpointFormatControl
: 
 - audioenginebaseapo.h
: 
 - APO_FLAG
: 
 - IAudioProcessingObject.GetInputChannelCount
: 
 - IAudioProcessingObject.GetLatency
: 
 - IAudioProcessingObject.GetRegistrationProperties
: 
 - IAudioProcessingObject.Initialize
: 
 - IAudioProcessingObject.IsInputFormatSupported
: 
 - IAudioProcessingObject.IsOutputFormatSupported
: 
 - IAudioProcessingObject.Reset
: 
 - IAudioProcessingObjectConfiguration.LockForProcess
: 
 - IAudioProcessingObjectConfiguration.UnlockForProcess
: 
 - IAudioProcessingObjectRT.APOProcess
: 
 - IAudioProcessingObjectRT.CalcInputFrames
: 
 - IAudioProcessingObjectRT.CalcOutputFrames
: 
 - IAudioSystemEffects2.GetEffectsList
: 
 - IAudioSystemEffectsCustomFormats.GetFormat
: 
 - IAudioSystemEffectsCustomFormats.GetFormatCount
: 
 - IAudioSystemEffectsCustomFormats.GetFormatRepresentation
: 
 - IAudioProcessingObject
: 
 - IAudioProcessingObjectConfiguration
: 
 - IAudioProcessingObjectRT
: 
 - IAudioSystemEffects2
: 
 - IAudioSystemEffectsCustomFormats
: 
 - APOInitBaseStruct
: 
 - APOInitSystemEffects
: 
 - APOInitSystemEffects2
: 
 - APO_REG_PROPERTIES
: 
 - __MIDL___MIDL_itf_audioenginebaseapo_0000_0007_0001
: 
 - audioengineendpoint.h
: 
 - AE_POSITION_FLAGS
: 
 - IAudioDeviceEndpoint.GetEventDrivenCapable
: 
 - IAudioDeviceEndpoint.GetRTCaps
: 
 - IAudioDeviceEndpoint.SetBuffer
: 
 - IAudioDeviceEndpoint.WriteExclusiveModeParametersToSharedMemory
: 
 - IAudioEndpoint.GetFrameFormat
: 
 - IAudioEndpoint.GetFramesPerPacket
: 
 - IAudioEndpoint.GetLatency
: 
 - IAudioEndpoint.SetEventHandle
: 
 - IAudioEndpoint.SetStreamFlags
: 
 - IAudioEndpointControl.Reset
: 
 - IAudioEndpointControl.Start
: 
 - IAudioEndpointControl.Stop
: 
 - IAudioEndpointLastBufferControl.IsLastBufferControlSupported
: 
 - IAudioEndpointLastBufferControl.ReleaseOutputDataPointerForLastBuffer
: 
 - IAudioEndpointOffloadStreamMeter.GetMeterChannelCount
: 
 - IAudioEndpointOffloadStreamMeter.GetMeteringData
: 
 - IAudioEndpointOffloadStreamMute.GetMute
: 
 - IAudioEndpointOffloadStreamMute.SetMute
: 
 - IAudioEndpointOffloadStreamVolume.GetChannelVolumes
: 
 - IAudioEndpointOffloadStreamVolume.GetVolumeChannelCount
: 
 - IAudioEndpointOffloadStreamVolume.SetChannelVolumes
: 
 - IAudioEndpointRT.GetCurrentPadding
: 
 - IAudioEndpointRT.ProcessingComplete
: 
 - IAudioEndpointRT.SetPinActive
: 
 - IAudioEndpointRT.SetPinInactive
: 
 - IAudioInputEndpointRT.GetInputDataPointer
: 
 - IAudioInputEndpointRT.PulseEndpoint
: 
 - IAudioInputEndpointRT.ReleaseInputDataPointer
: 
 - IAudioLfxControl.GetLocalEffectsState
: 
 - IAudioLfxControl.SetLocalEffectsState
: 
 - IAudioOutputEndpointRT.GetOutputDataPointer
: 
 - IAudioOutputEndpointRT.PulseEndpoint
: 
 - IAudioOutputEndpointRT.ReleaseOutputDataPointer
: 
 - IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount
: 
 - IHardwareAudioEngineBase.GetEngineFormat
: 
 - IHardwareAudioEngineBase.GetGfxState
: 
 - IHardwareAudioEngineBase.SetEngineDeviceFormat
: 
 - IHardwareAudioEngineBase.SetGfxState
: 
 - IAudioDeviceEndpoint
: 
 - IAudioEndpoint
: 
 - IAudioEndpointControl
: 
 - IAudioEndpointLastBufferControl
: 
 - IAudioEndpointOffloadStreamMeter
: 
 - IAudioEndpointOffloadStreamMute
: 
 - IAudioEndpointOffloadStreamVolume
: 
 - IAudioEndpointRT
: 
 - IAudioInputEndpointRT
: 
 - IAudioLfxControl
: 
 - IAudioOutputEndpointRT
: 
 - IHardwareAudioEngineBase
: 
 - AE_CURRENT_POSITION
: 
 - CreateAudioMediaType
: 
 - CreateAudioMediaTypeFromUncompressedAudioFormat
: 
 - audiomediatype.h
: 
 - IAudioMediaType.GetAudioFormat
: 
 - IAudioMediaType.GetUncompressedAudioFormat
: 
 - IAudioMediaType.IsCompressedFormat
: 
 - IAudioMediaType.IsEqual
: 
 - IAudioMediaType
: 
 - _UNCOMPRESSEDAUDIOFORMAT
: 
 - audiopolicy.h
: 
 - IAudioSessionControl.GetDisplayName
: 
 - IAudioSessionControl.GetGroupingParam
: 
 - IAudioSessionControl.GetIconPath
: 
 - IAudioSessionControl.GetState
: 
 - IAudioSessionControl.RegisterAudioSessionNotification
: 
 - IAudioSessionControl.SetDisplayName
: 
 - IAudioSessionControl.SetGroupingParam
: 
 - IAudioSessionControl.SetIconPath
: 
 - IAudioSessionControl.UnregisterAudioSessionNotification
: 
 - IAudioSessionControl2.GetProcessId
: 
 - IAudioSessionControl2.GetSessionIdentifier
: 
 - IAudioSessionControl2.GetSessionInstanceIdentifier
: 
 - IAudioSessionControl2.IsSystemSoundsSession
: 
 - IAudioSessionControl2.SetDuckingPreference
: 
 - IAudioSessionEnumerator.GetCount
: 
 - IAudioSessionEnumerator.GetSession
: 
 - IAudioSessionEvents.OnChannelVolumeChanged
: 
 - IAudioSessionEvents.OnDisplayNameChanged
: 
 - IAudioSessionEvents.OnGroupingParamChanged
: 
 - IAudioSessionEvents.OnIconPathChanged
: 
 - IAudioSessionEvents.OnSessionDisconnected
: 
 - IAudioSessionEvents.OnSimpleVolumeChanged
: 
 - IAudioSessionEvents.OnStateChanged
: 
 - IAudioSessionManager.GetAudioSessionControl
: 
 - IAudioSessionManager.GetSimpleAudioVolume
: 
 - IAudioSessionManager2.GetSessionEnumerator
: 
 - IAudioSessionManager2.RegisterDuckNotification
: 
 - IAudioSessionManager2.RegisterSessionNotification
: 
 - IAudioSessionManager2.UnregisterDuckNotification
: 
 - IAudioSessionManager2.UnregisterSessionNotification
: 
 - IAudioSessionNotification.OnSessionCreated
: 
 - IAudioVolumeDuckNotification.OnVolumeDuckNotification
: 
 - IAudioVolumeDuckNotification.OnVolumeUnduckNotification
: 
 - IAudioSessionControl
: 
 - IAudioSessionControl2
: 
 - IAudioSessionEnumerator
: 
 - IAudioSessionEvents
: 
 - IAudioSessionManager
: 
 - IAudioSessionManager2
: 
 - IAudioSessionNotification
: 
 - IAudioVolumeDuckNotification
: 
 - audiosessiontypes.h
: 
 - _AUDCLNT_SHAREMODE
: 
 - _AudioSessionState
: 
 - _AUDIO_STREAM_CATEGORY
: 
 - austream.h
: 
 - IAudioData.GetFormat
: 
 - IAudioData.SetFormat
: 
 - IAudioMediaStream.CreateSample
: 
 - IAudioMediaStream.GetFormat
: 
 - IAudioMediaStream.SetFormat
: 
 - IAudioStreamSample.GetAudioData
: 
 - IMemoryData.GetInfo
: 
 - IMemoryData.SetActual
: 
 - IMemoryData.SetBuffer
: 
 - IAudioData
: 
 - IAudioMediaStream
: 
 - IAudioStreamSample
: 
 - IMemoryData
: 
 - authif.h
: 
 - PRADIUS_EXTENSION_FREE_ATTRIBUTES
: 
 - PRADIUS_EXTENSION_INIT
: 
 - PRADIUS_EXTENSION_PROCESS
: 
 - PRADIUS_EXTENSION_PROCESS_2
: 
 - PRADIUS_EXTENSION_PROCESS_EX
: 
 - PRADIUS_EXTENSION_TERM
: 
 - _RADIUS_ACTION
: 
 - _RADIUS_ATTRIBUTE_TYPE
: 
 - _RADIUS_AUTHENTICATION_PROVIDER
: 
 - _RADIUS_CODE
: 
 - _RADIUS_DATA_TYPE
: 
 - _RADIUS_EXTENSION_POINT
: 
 - _RADIUS_REJECT_REASON_CODE
: 
 - _RADIUS_ATTRIBUTE
: 
 - _RADIUS_ATTRIBUTE_ARRAY
: 
 - _RADIUS_EXTENSION_CONTROL_BLOCK
: 
 - _RADIUS_VSA_FORMAT
: 
 - authz.h
: 
 - AUTHZ_SECURITY_ATTRIBUTE_OPERATION
: 
 - AUTHZ_SID_OPERATION
: 
 - _AUTHZ_CONTEXT_INFORMATION_CLASS
: 
 - AuthzAccessCheck
: 
 - AuthzAddSidsToContext
: 
 - AuthzCachedAccessCheck
: 
 - AuthzEnumerateSecurityEventSources
: 
 - AuthzFreeAuditEvent
: 
 - AuthzFreeCentralAccessPolicyCache
: 
 - AuthzFreeContext
: 
 - AuthzFreeHandle
: 
 - AuthzFreeResourceManager
: 
 - AuthzGetInformationFromContext
: 
 - AuthzInitializeCompoundContext
: 
 - AuthzInitializeContextFromAuthzContext
: 
 - AuthzInitializeContextFromSid
: 
 - AuthzInitializeContextFromToken
: 
 - AuthzInitializeObjectAccessAuditEvent
: 
 - AuthzInitializeObjectAccessAuditEvent2
: 
 - AuthzInitializeRemoteResourceManager
: 
 - AuthzInitializeResourceManager
: 
 - AuthzInitializeResourceManagerEx
: 
 - AuthzInstallSecurityEventSource
: 
 - AuthzModifyClaims
: 
 - AuthzModifySecurityAttributes
: 
 - AuthzModifySids
: 
 - AuthzOpenObjectAudit
: 
 - AuthzRegisterCapChangeNotification
: 
 - AuthzRegisterSecurityEventSource
: 
 - AuthzReportSecurityEvent
: 
 - AuthzReportSecurityEventFromParams
: 
 - AuthzSetAppContainerInformation
: 
 - AuthzUninstallSecurityEventSource
: 
 - AuthzUnregisterCapChangeNotification
: 
 - AuthzUnregisterSecurityEventSource
: 
 - _AUTHZ_ACCESS_REPLY
: 
 - _AUTHZ_ACCESS_REQUEST
: 
 - _AUTHZ_INIT_INFO
: 
 - _AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
: 
 - _AUTHZ_RPC_INIT_INFO_CLIENT
: 
 - _AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
: 
 - _AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
: 
 - _AUTHZ_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
: 
 - _AUTHZ_SECURITY_ATTRIBUTE_V1
: 
 - _AUTHZ_SOURCE_SCHEMA_REGISTRATION
: 
 - AuxUlibInitialize
: 
 - AuxUlibIsDLLSynchronizationHeld
: 
 - AuxUlibSetSystemFileCacheSize
: 
 - avifmt.h
: 
 - AVIPALCHANGE
: 
 - AVIStreamHeader
: 
 - aviriff.h
: 
 - tagTIMECODE_SAMPLE
: 
 - _avimainheader
: 
 - _avimetaindex
: 
 - _avioldindex
: 
 - _avistdindex
: 
 - _avistdindex_entry
: 
 - _avistreamheader
: 
 - _avisuperindex
: 
 - avrfsdk.h
: 
 - AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK
: 
 - AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
: 
 - AVRF_RESOURCE_ENUMERATE_CALLBACK
: 
 - eAvrfResourceTypes
: 
 - eHANDLE_TRACE_OPERATIONS
: 
 - eHeapAllocationState
: 
 - eHeapEnumerationLevel
: 
 - eUserAllocationState
: 
 - VerifierEnumerateResource
: 
 - VerifierIsPerUserSettingsEnabled
: 
 - _AVRF_BACKTRACE_INFORMATION
: 
 - _AVRF_HANDLE_OPERATION
: 
 - _AVRF_HEAP_ALLOCATION
: 
 - AvQuerySystemResponsiveness
: 
 - AvRevertMmThreadCharacteristics
: 
 - AvRtCreateThreadOrderingGroup
: 
 - AvRtCreateThreadOrderingGroupExA
: 
 - AvRtCreateThreadOrderingGroupExW
: 
 - AvRtDeleteThreadOrderingGroup
: 
 - AvRtJoinThreadOrderingGroup
: 
 - AvRtLeaveThreadOrderingGroup
: 
 - AvRtWaitOnThreadOrderingGroup
: 
 - AvSetMmMaxThreadCharacteristicsA
: 
 - AvSetMmMaxThreadCharacteristicsW
: 
 - AvSetMmThreadCharacteristicsA
: 
 - AvSetMmThreadCharacteristicsW
: 
 - AvSetMmThreadPriority
: 
 - azroles.h
: 
 - tagAZ_PROP_CONSTANTS
: 
 - IAzApplication.AddDelegatedPolicyUser
: 
 - IAzApplication.AddDelegatedPolicyUserName
: 
 - IAzApplication.AddPolicyAdministrator
: 
 - IAzApplication.AddPolicyAdministratorName
: 
 - IAzApplication.AddPolicyReader
: 
 - IAzApplication.AddPolicyReaderName
: 
 - IAzApplication.AddPropertyItem
: 
 - IAzApplication.CreateApplicationGroup
: 
 - IAzApplication.CreateOperation
: 
 - IAzApplication.CreateRole
: 
 - IAzApplication.CreateScope
: 
 - IAzApplication.CreateTask
: 
 - IAzApplication.DeleteApplicationGroup
: 
 - IAzApplication.DeleteDelegatedPolicyUser
: 
 - IAzApplication.DeleteDelegatedPolicyUserName
: 
 - IAzApplication.DeleteOperation
: 
 - IAzApplication.DeletePolicyAdministrator
: 
 - IAzApplication.DeletePolicyAdministratorName
: 
 - IAzApplication.DeletePolicyReader
: 
 - IAzApplication.DeletePolicyReaderName
: 
 - IAzApplication.DeletePropertyItem
: 
 - IAzApplication.DeleteRole
: 
 - IAzApplication.DeleteScope
: 
 - IAzApplication.DeleteTask
: 
 - IAzApplication.GetProperty
: 
 - IAzApplication.get_ApplicationData
: 
 - IAzApplication.get_ApplicationGroups
: 
 - IAzApplication.get_ApplyStoreSacl
: 
 - IAzApplication.get_AuthzInterfaceClsid
: 
 - IAzApplication.get_DelegatedPolicyUsers
: 
 - IAzApplication.get_DelegatedPolicyUsersName
: 
 - IAzApplication.get_Description
: 
 - IAzApplication.get_GenerateAudits
: 
 - IAzApplication.get_Name
: 
 - IAzApplication.get_Operations
: 
 - IAzApplication.get_PolicyAdministrators
: 
 - IAzApplication.get_PolicyAdministratorsName
: 
 - IAzApplication.get_PolicyReaders
: 
 - IAzApplication.get_PolicyReadersName
: 
 - IAzApplication.get_Roles
: 
 - IAzApplication.get_Scopes
: 
 - IAzApplication.get_Tasks
: 
 - IAzApplication.get_Version
: 
 - IAzApplication.get_Writable
: 
 - IAzApplication.InitializeClientContextFromName
: 
 - IAzApplication.InitializeClientContextFromStringSid
: 
 - IAzApplication.InitializeClientContextFromToken
: 
 - IAzApplication.OpenApplicationGroup
: 
 - IAzApplication.OpenOperation
: 
 - IAzApplication.OpenRole
: 
 - IAzApplication.OpenScope
: 
 - IAzApplication.OpenTask
: 
 - IAzApplication.put_ApplicationData
: 
 - IAzApplication.put_ApplyStoreSacl
: 
 - IAzApplication.put_AuthzInterfaceClsid
: 
 - IAzApplication.put_Description
: 
 - IAzApplication.put_GenerateAudits
: 
 - IAzApplication.put_Name
: 
 - IAzApplication.put_Version
: 
 - IAzApplication.SetProperty
: 
 - IAzApplication.Submit
: 
 - IAzApplication2.InitializeClientContext2
: 
 - IAzApplication2.InitializeClientContextFromToken2
: 
 - IAzApplication3.CreateRoleAssignment
: 
 - IAzApplication3.CreateRoleDefinition
: 
 - IAzApplication3.CreateScope2
: 
 - IAzApplication3.DeleteRoleAssignment
: 
 - IAzApplication3.DeleteRoleDefinition
: 
 - IAzApplication3.DeleteScope2
: 
 - IAzApplication3.get_BizRulesEnabled
: 
 - IAzApplication3.get_RoleAssignments
: 
 - IAzApplication3.get_RoleDefinitions
: 
 - IAzApplication3.OpenRoleAssignment
: 
 - IAzApplication3.OpenRoleDefinition
: 
 - IAzApplication3.OpenScope2
: 
 - IAzApplication3.put_BizRulesEnabled
: 
 - IAzApplication3.ScopeExists
: 
 - IAzApplicationGroup.AddAppMember
: 
 - IAzApplicationGroup.AddAppNonMember
: 
 - IAzApplicationGroup.AddMember
: 
 - IAzApplicationGroup.AddMemberName
: 
 - IAzApplicationGroup.AddNonMember
: 
 - IAzApplicationGroup.AddNonMemberName
: 
 - IAzApplicationGroup.AddPropertyItem
: 
 - IAzApplicationGroup.DeleteAppMember
: 
 - IAzApplicationGroup.DeleteAppNonMember
: 
 - IAzApplicationGroup.DeleteMember
: 
 - IAzApplicationGroup.DeleteMemberName
: 
 - IAzApplicationGroup.DeleteNonMember
: 
 - IAzApplicationGroup.DeleteNonMemberName
: 
 - IAzApplicationGroup.DeletePropertyItem
: 
 - IAzApplicationGroup.GetProperty
: 
 - IAzApplicationGroup.get_AppMembers
: 
 - IAzApplicationGroup.get_AppNonMembers
: 
 - IAzApplicationGroup.get_Description
: 
 - IAzApplicationGroup.get_LdapQuery
: 
 - IAzApplicationGroup.get_Members
: 
 - IAzApplicationGroup.get_MembersName
: 
 - IAzApplicationGroup.get_Name
: 
 - IAzApplicationGroup.get_NonMembers
: 
 - IAzApplicationGroup.get_NonMembersName
: 
 - IAzApplicationGroup.get_Type
: 
 - IAzApplicationGroup.get_Writable
: 
 - IAzApplicationGroup.put_Description
: 
 - IAzApplicationGroup.put_LdapQuery
: 
 - IAzApplicationGroup.put_Name
: 
 - IAzApplicationGroup.put_Type
: 
 - IAzApplicationGroup.SetProperty
: 
 - IAzApplicationGroup.Submit
: 
 - IAzApplicationGroup2.get_BizRule
: 
 - IAzApplicationGroup2.get_BizRuleImportedPath
: 
 - IAzApplicationGroup2.get_BizRuleLanguage
: 
 - IAzApplicationGroup2.put_BizRule
: 
 - IAzApplicationGroup2.put_BizRuleImportedPath
: 
 - IAzApplicationGroup2.put_BizRuleLanguage
: 
 - IAzApplicationGroup2.RoleAssignments
: 
 - IAzApplicationGroups.get_Count
: 
 - IAzApplicationGroups.get_Item
: 
 - IAzApplicationGroups.get__NewEnum
: 
 - IAzApplications.get_Count
: 
 - IAzApplications.get_Item
: 
 - IAzApplications.get__NewEnum
: 
 - IAzAuthorizationStore.AddDelegatedPolicyUser
: 
 - IAzAuthorizationStore.AddDelegatedPolicyUserName
: 
 - IAzAuthorizationStore.AddPolicyAdministrator
: 
 - IAzAuthorizationStore.AddPolicyAdministratorName
: 
 - IAzAuthorizationStore.AddPolicyReader
: 
 - IAzAuthorizationStore.AddPolicyReaderName
: 
 - IAzAuthorizationStore.AddPropertyItem
: 
 - IAzAuthorizationStore.CloseApplication
: 
 - IAzAuthorizationStore.CreateApplication
: 
 - IAzAuthorizationStore.CreateApplicationGroup
: 
 - IAzAuthorizationStore.Delete
: 
 - IAzAuthorizationStore.DeleteApplication
: 
 - IAzAuthorizationStore.DeleteApplicationGroup
: 
 - IAzAuthorizationStore.DeleteDelegatedPolicyUser
: 
 - IAzAuthorizationStore.DeleteDelegatedPolicyUserName
: 
 - IAzAuthorizationStore.DeletePolicyAdministrator
: 
 - IAzAuthorizationStore.DeletePolicyAdministratorName
: 
 - IAzAuthorizationStore.DeletePolicyReader
: 
 - IAzAuthorizationStore.DeletePolicyReaderName
: 
 - IAzAuthorizationStore.DeletePropertyItem
: 
 - IAzAuthorizationStore.GetProperty
: 
 - IAzAuthorizationStore.get_ApplicationData
: 
 - IAzAuthorizationStore.get_ApplicationGroups
: 
 - IAzAuthorizationStore.get_Applications
: 
 - IAzAuthorizationStore.get_ApplyStoreSacl
: 
 - IAzAuthorizationStore.get_DelegatedPolicyUsers
: 
 - IAzAuthorizationStore.get_DelegatedPolicyUsersName
: 
 - IAzAuthorizationStore.get_Description
: 
 - IAzAuthorizationStore.get_DomainTimeout
: 
 - IAzAuthorizationStore.get_GenerateAudits
: 
 - IAzAuthorizationStore.get_MaxScriptEngines
: 
 - IAzAuthorizationStore.get_PolicyAdministrators
: 
 - IAzAuthorizationStore.get_PolicyAdministratorsName
: 
 - IAzAuthorizationStore.get_PolicyReaders
: 
 - IAzAuthorizationStore.get_PolicyReadersName
: 
 - IAzAuthorizationStore.get_ScriptEngineTimeout
: 
 - IAzAuthorizationStore.get_TargetMachine
: 
 - IAzAuthorizationStore.get_Writable
: 
 - IAzAuthorizationStore.Initialize
: 
 - IAzAuthorizationStore.OpenApplication
: 
 - IAzAuthorizationStore.OpenApplicationGroup
: 
 - IAzAuthorizationStore.put_ApplicationData
: 
 - IAzAuthorizationStore.put_ApplyStoreSacl
: 
 - IAzAuthorizationStore.put_Description
: 
 - IAzAuthorizationStore.put_DomainTimeout
: 
 - IAzAuthorizationStore.put_GenerateAudits
: 
 - IAzAuthorizationStore.put_MaxScriptEngines
: 
 - IAzAuthorizationStore.put_ScriptEngineTimeout
: 
 - IAzAuthorizationStore.SetProperty
: 
 - IAzAuthorizationStore.Submit
: 
 - IAzAuthorizationStore.UpdateCache
: 
 - IAzAuthorizationStore2.CreateApplication2
: 
 - IAzAuthorizationStore2.OpenApplication2
: 
 - IAzAuthorizationStore3.BizruleGroupSupported
: 
 - IAzAuthorizationStore3.GetSchemaVersion
: 
 - IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported
: 
 - IAzAuthorizationStore3.IsUpdateNeeded
: 
 - IAzAuthorizationStore3.UpgradeStoresFunctionalLevel
: 
 - IAzBizRuleContext.GetParameter
: 
 - IAzBizRuleContext.get_BusinessRuleString
: 
 - IAzBizRuleContext.put_BusinessRuleResult
: 
 - IAzBizRuleContext.put_BusinessRuleString
: 
 - IAzBizRuleInterfaces.AddInterface
: 
 - IAzBizRuleInterfaces.AddInterfaces
: 
 - IAzBizRuleInterfaces.GetInterfaceValue
: 
 - IAzBizRuleInterfaces.get_Count
: 
 - IAzBizRuleInterfaces.Remove
: 
 - IAzBizRuleInterfaces.RemoveAll
: 
 - IAzBizRuleParameters.AddParameter
: 
 - IAzBizRuleParameters.AddParameters
: 
 - IAzBizRuleParameters.GetParameterValue
: 
 - IAzBizRuleParameters.get_Count
: 
 - IAzBizRuleParameters.Remove
: 
 - IAzBizRuleParameters.RemoveAll
: 
 - IAzClientContext.AccessCheck
: 
 - IAzClientContext.GetBusinessRuleString
: 
 - IAzClientContext.GetProperty
: 
 - IAzClientContext.GetRoles
: 
 - IAzClientContext.get_RoleForAccessCheck
: 
 - IAzClientContext.get_UserCanonical
: 
 - IAzClientContext.get_UserDisplay
: 
 - IAzClientContext.get_UserDn
: 
 - IAzClientContext.get_UserDnsSamCompat
: 
 - IAzClientContext.get_UserGuid
: 
 - IAzClientContext.get_UserSamCompat
: 
 - IAzClientContext.get_UserUpn
: 
 - IAzClientContext.put_RoleForAccessCheck
: 
 - IAzClientContext2.AddApplicationGroups
: 
 - IAzClientContext2.AddRoles
: 
 - IAzClientContext2.AddStringSids
: 
 - IAzClientContext2.GetAssignedScopesPage
: 
 - IAzClientContext2.get_LDAPQueryDN
: 
 - IAzClientContext2.put_LDAPQueryDN
: 
 - IAzClientContext3.AccessCheck2
: 
 - IAzClientContext3.GetGroups
: 
 - IAzClientContext3.GetOperations
: 
 - IAzClientContext3.GetTasks
: 
 - IAzClientContext3.get_BizRuleInterfaces
: 
 - IAzClientContext3.get_BizRuleParameters
: 
 - IAzClientContext3.get_Sids
: 
 - IAzClientContext3.IsInRoleAssignment
: 
 - IAzNameResolver.NameFromSid
: 
 - IAzNameResolver.NamesFromSids
: 
 - IAzObjectPicker.GetPrincipals
: 
 - IAzObjectPicker.get_Name
: 
 - IAzOperation.GetProperty
: 
 - IAzOperation.get_ApplicationData
: 
 - IAzOperation.get_Description
: 
 - IAzOperation.get_Name
: 
 - IAzOperation.get_OperationID
: 
 - IAzOperation.get_Writable
: 
 - IAzOperation.put_ApplicationData
: 
 - IAzOperation.put_Description
: 
 - IAzOperation.put_Name
: 
 - IAzOperation.put_OperationID
: 
 - IAzOperation.SetProperty
: 
 - IAzOperation.Submit
: 
 - IAzOperation2.RoleAssignments
: 
 - IAzOperations.get_Count
: 
 - IAzOperations.get_Item
: 
 - IAzOperations.get__NewEnum
: 
 - IAzPrincipalLocator.get_NameResolver
: 
 - IAzPrincipalLocator.get_ObjectPicker
: 
 - IAzRole.AddAppMember
: 
 - IAzRole.AddMember
: 
 - IAzRole.AddMemberName
: 
 - IAzRole.AddOperation
: 
 - IAzRole.AddPropertyItem
: 
 - IAzRole.AddTask
: 
 - IAzRole.DeleteAppMember
: 
 - IAzRole.DeleteMember
: 
 - IAzRole.DeleteMemberName
: 
 - IAzRole.DeleteOperation
: 
 - IAzRole.DeletePropertyItem
: 
 - IAzRole.DeleteTask
: 
 - IAzRole.GetProperty
: 
 - IAzRole.get_ApplicationData
: 
 - IAzRole.get_AppMembers
: 
 - IAzRole.get_Description
: 
 - IAzRole.get_Members
: 
 - IAzRole.get_MembersName
: 
 - IAzRole.get_Name
: 
 - IAzRole.get_Operations
: 
 - IAzRole.get_Tasks
: 
 - IAzRole.get_Writable
: 
 - IAzRole.put_ApplicationData
: 
 - IAzRole.put_Description
: 
 - IAzRole.put_Name
: 
 - IAzRole.SetProperty
: 
 - IAzRole.Submit
: 
 - IAzRoleAssignment.AddRoleDefinition
: 
 - IAzRoleAssignment.DeleteRoleDefinition
: 
 - IAzRoleAssignment.get_RoleDefinitions
: 
 - IAzRoleAssignment.get_Scope
: 
 - IAzRoleAssignments.get_Count
: 
 - IAzRoleAssignments.get_Item
: 
 - IAzRoleAssignments.get__NewEnum
: 
 - IAzRoleDefinition.AddRoleDefinition
: 
 - IAzRoleDefinition.DeleteRoleDefinition
: 
 - IAzRoleDefinition.get_RoleDefinitions
: 
 - IAzRoleDefinition.RoleAssignments
: 
 - IAzRoleDefinitions.get_Count
: 
 - IAzRoleDefinitions.get_Item
: 
 - IAzRoleDefinitions.get__NewEnum
: 
 - IAzRoles.get_Count
: 
 - IAzRoles.get_Item
: 
 - IAzRoles.get__NewEnum
: 
 - IAzScope.AddPolicyAdministrator
: 
 - IAzScope.AddPolicyAdministratorName
: 
 - IAzScope.AddPolicyReader
: 
 - IAzScope.AddPolicyReaderName
: 
 - IAzScope.AddPropertyItem
: 
 - IAzScope.CreateApplicationGroup
: 
 - IAzScope.CreateRole
: 
 - IAzScope.CreateTask
: 
 - IAzScope.DeleteApplicationGroup
: 
 - IAzScope.DeletePolicyAdministrator
: 
 - IAzScope.DeletePolicyAdministratorName
: 
 - IAzScope.DeletePolicyReader
: 
 - IAzScope.DeletePolicyReaderName
: 
 - IAzScope.DeletePropertyItem
: 
 - IAzScope.DeleteRole
: 
 - IAzScope.DeleteTask
: 
 - IAzScope.GetProperty
: 
 - IAzScope.get_ApplicationData
: 
 - IAzScope.get_ApplicationGroups
: 
 - IAzScope.get_BizrulesWritable
: 
 - IAzScope.get_CanBeDelegated
: 
 - IAzScope.get_Description
: 
 - IAzScope.get_Name
: 
 - IAzScope.get_PolicyAdministrators
: 
 - IAzScope.get_PolicyAdministratorsName
: 
 - IAzScope.get_PolicyReaders
: 
 - IAzScope.get_PolicyReadersName
: 
 - IAzScope.get_Roles
: 
 - IAzScope.get_Tasks
: 
 - IAzScope.get_Writable
: 
 - IAzScope.OpenApplicationGroup
: 
 - IAzScope.OpenRole
: 
 - IAzScope.OpenTask
: 
 - IAzScope.put_ApplicationData
: 
 - IAzScope.put_Description
: 
 - IAzScope.put_Name
: 
 - IAzScope.SetProperty
: 
 - IAzScope.Submit
: 
 - IAzScope2.CreateRoleAssignment
: 
 - IAzScope2.CreateRoleDefinition
: 
 - IAzScope2.DeleteRoleAssignment
: 
 - IAzScope2.DeleteRoleDefinition
: 
 - IAzScope2.get_RoleAssignments
: 
 - IAzScope2.get_RoleDefinitions
: 
 - IAzScope2.OpenRoleAssignment
: 
 - IAzScope2.OpenRoleDefinition
: 
 - IAzScopes.get_Count
: 
 - IAzScopes.get_Item
: 
 - IAzScopes.get__NewEnum
: 
 - IAzTask.AddOperation
: 
 - IAzTask.AddPropertyItem
: 
 - IAzTask.AddTask
: 
 - IAzTask.DeleteOperation
: 
 - IAzTask.DeletePropertyItem
: 
 - IAzTask.DeleteTask
: 
 - IAzTask.GetProperty
: 
 - IAzTask.get_ApplicationData
: 
 - IAzTask.get_BizRule
: 
 - IAzTask.get_BizRuleImportedPath
: 
 - IAzTask.get_BizRuleLanguage
: 
 - IAzTask.get_Description
: 
 - IAzTask.get_IsRoleDefinition
: 
 - IAzTask.get_Name
: 
 - IAzTask.get_Operations
: 
 - IAzTask.get_Tasks
: 
 - IAzTask.get_Writable
: 
 - IAzTask.put_ApplicationData
: 
 - IAzTask.put_BizRule
: 
 - IAzTask.put_BizRuleImportedPath
: 
 - IAzTask.put_BizRuleLanguage
: 
 - IAzTask.put_Description
: 
 - IAzTask.put_IsRoleDefinition
: 
 - IAzTask.put_Name
: 
 - IAzTask.SetProperty
: 
 - IAzTask.Submit
: 
 - IAzTask2.RoleAssignments
: 
 - IAzTasks.get_Count
: 
 - IAzTasks.get_Item
: 
 - IAzTasks.get__NewEnum
: 
 - IAzApplication
: 
 - IAzApplication2
: 
 - IAzApplication3
: 
 - IAzApplicationGroup
: 
 - IAzApplicationGroup2
: 
 - IAzApplicationGroups
: 
 - IAzApplications
: 
 - IAzAuthorizationStore
: 
 - IAzAuthorizationStore2
: 
 - IAzAuthorizationStore3
: 
 - IAzBizRuleContext
: 
 - IAzBizRuleInterfaces
: 
 - IAzBizRuleParameters
: 
 - IAzClientContext
: 
 - IAzClientContext2
: 
 - IAzClientContext3
: 
 - IAzNameResolver
: 
 - IAzObjectPicker
: 
 - IAzOperation
: 
 - IAzOperation2
: 
 - IAzOperations
: 
 - IAzPrincipalLocator
: 
 - IAzRole
: 
 - IAzRoleAssignment
: 
 - IAzRoleAssignments
: 
 - IAzRoleDefinition
: 
 - IAzRoleDefinitions
: 
 - IAzRoles
: 
 - IAzScope
: 
 - IAzScope2
: 
 - IAzScopes
: 
 - IAzTask
: 
 - IAzTask2
: 
 - IAzTasks
: 
 - AERT_Allocate
: 
 - AERT_Free
: 
 - batclass.h
: 
 - BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK
: 
 - BCLASS_QUERY_INFORMATION_CALLBACK
: 
 - BCLASS_QUERY_STATUS_CALLBACK
: 
 - BCLASS_QUERY_TAG_CALLBACK
: 
 - BCLASS_SET_INFORMATION_CALLBACK
: 
 - BCLASS_SET_STATUS_NOTIFY_CALLBACK
: 
 - BatteryClassInitializeDevice
: 
 - BatteryClassIoctl
: 
 - BatteryClassQueryWmiDataBlock
: 
 - BatteryClassStatusNotify
: 
 - BatteryClassSystemControl
: 
 - BatteryClassUnload
: 
 - BATTERY_MINIPORT_INFO
: 
 - BATTERY_MINIPORT_INFO_V1_1
: 
 - BATTERY_NOTIFY
: 
 - _BATTERY_TAG_CHANGE
: 
 - _BATTERY_WMI_CYCLE_COUNT
: 
 - _BATTERY_WMI_FULL_CHARGED_CAPACITY
: 
 - _BATTERY_WMI_RUNTIME
: 
 - _BATTERY_WMI_STATIC_DATA
: 
 - _BATTERY_WMI_STATUS
: 
 - _BATTERY_WMI_STATUS_CHANGE
: 
 - _BATTERY_WMI_TEMPERATURE
: 
 - bcrypt.h
: 
 - BCRYPT_HASH_OPERATION_TYPE
: 
 - BCRYPT_MULTI_OPERATION_TYPE
: 
 - DSAFIPSVERSION_ENUM
: 
 - HASHALGORITHM_ENUM
: 
 - BCryptAddContextFunction
: 
 - BCryptCloseAlgorithmProvider
: 
 - BCryptConfigureContext
: 
 - BCryptConfigureContextFunction
: 
 - BCryptCreateContext
: 
 - BCryptCreateHash
: 
 - BCryptCreateMultiHash
: 
 - BCryptDecrypt
: 
 - BCryptDeleteContext
: 
 - BCryptDeriveKey
: 
 - BCryptDeriveKeyCapi
: 
 - BCryptDeriveKeyPBKDF2
: 
 - BCryptDestroyHash
: 
 - BCryptDestroyKey
: 
 - BCryptDestroySecret
: 
 - BCryptDuplicateHash
: 
 - BCryptDuplicateKey
: 
 - BCryptEncrypt
: 
 - BCryptEnumAlgorithms
: 
 - BCryptEnumContextFunctionProviders
: 
 - BCryptEnumContextFunctions
: 
 - BCryptEnumContexts
: 
 - BCryptEnumProviders
: 
 - BCryptEnumRegisteredProviders
: 
 - BCryptExportKey
: 
 - BCryptFinalizeKeyPair
: 
 - BCryptFinishHash
: 
 - BCryptFreeBuffer
: 
 - BCryptGenerateKeyPair
: 
 - BCryptGenerateSymmetricKey
: 
 - BCryptGenRandom
: 
 - BCryptGetFipsAlgorithmMode
: 
 - BCryptGetProperty
: 
 - BCryptHash
: 
 - BCryptHashData
: 
 - BCryptImportKey
: 
 - BCryptImportKeyPair
: 
 - BCryptKeyDerivation
: 
 - BCryptOpenAlgorithmProvider
: 
 - BCryptProcessMultiOperations
: 
 - BCryptQueryContextConfiguration
: 
 - BCryptQueryContextFunctionConfiguration
: 
 - BCryptQueryContextFunctionProperty
: 
 - BCryptQueryProviderRegistration
: 
 - BCryptRegisterConfigChangeNotify
: 
 - BCryptRemoveContextFunction
: 
 - BCryptResolveProviders
: 
 - BCryptSecretAgreement
: 
 - BCryptSetContextFunctionProperty
: 
 - BCryptSetProperty
: 
 - BCryptSignHash
: 
 - BCryptUnregisterConfigChangeNotify
: 
 - BCryptVerifySignature
: 
 - BCRYPT_INIT_AUTH_MODE_INFO
: 
 - _BCRYPT_ALGORITHM_IDENTIFIER
: 
 - _BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
: 
 - _BCRYPT_DH_KEY_BLOB
: 
 - _BCRYPT_DH_PARAMETER_HEADER
: 
 - _BCRYPT_DSA_KEY_BLOB
: 
 - _BCRYPT_DSA_KEY_BLOB_V2
: 
 - _BCRYPT_DSA_PARAMETER_HEADER
: 
 - _BCRYPT_DSA_PARAMETER_HEADER_V2
: 
 - _BCRYPT_ECCKEY_BLOB
: 
 - _BCRYPT_INTERFACE_VERSION
: 
 - _BCRYPT_KEY_BLOB
: 
 - _BCRYPT_KEY_DATA_BLOB_HEADER
: 
 - _BCRYPT_MULTI_HASH_OPERATION
: 
 - _BCRYPT_MULTI_OBJECT_LENGTH_STRUCT
: 
 - _BCRYPT_OAEP_PADDING_INFO
: 
 - _BCRYPT_OID
: 
 - _BCRYPT_OID_LIST
: 
 - _BCRYPT_PKCS1_PADDING_INFO
: 
 - _BCRYPT_PROVIDER_NAME
: 
 - _BCRYPT_PSS_PADDING_INFO
: 
 - _BCRYPT_RSAKEY_BLOB
: 
 - _CRYPT_CONTEXTS
: 
 - _CRYPT_CONTEXT_CONFIG
: 
 - _CRYPT_CONTEXT_FUNCTIONS
: 
 - _CRYPT_CONTEXT_FUNCTION_CONFIG
: 
 - _CRYPT_CONTEXT_FUNCTION_PROVIDERS
: 
 - _CRYPT_IMAGE_REF
: 
 - _CRYPT_IMAGE_REG
: 
 - _CRYPT_INTERFACE_REG
: 
 - _CRYPT_PROPERTY_REF
: 
 - _CRYPT_PROVIDERS
: 
 - _CRYPT_PROVIDER_REF
: 
 - _CRYPT_PROVIDER_REFS
: 
 - _CRYPT_PROVIDER_REG
: 
 - __BCRYPT_KEY_LENGTHS_STRUCT
: 
 - bdaiface.h
: 
 - BDA_DrmPairingError
: 
 - SmartCardAssociationType
: 
 - SmartCardStatusType
: 
 - UICloseReasonType
: 
 - IBDA_AutoDemodulate.put_AutoDemodulate
: 
 - IBDA_AutoDemodulateEx.get_AuxInputCount
: 
 - IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes
: 
 - IBDA_AutoDemodulateEx.get_SupportedVideoFormats
: 
 - IBDA_AUX.EnumCapability
: 
 - IBDA_AUX.QueryCapabilities
: 
 - IBDA_ConditionalAccess.AddProgram
: 
 - IBDA_ConditionalAccess.GetModuleUI
: 
 - IBDA_ConditionalAccess.get_Entitlement
: 
 - IBDA_ConditionalAccess.get_SmartCardApplications
: 
 - IBDA_ConditionalAccess.get_SmartCardInfo
: 
 - IBDA_ConditionalAccess.get_SmartCardStatus
: 
 - IBDA_ConditionalAccess.InformUIClosed
: 
 - IBDA_ConditionalAccess.RemoveProgram
: 
 - IBDA_ConditionalAccess.SetProgram
: 
 - IBDA_ConditionalAccess.TuneByChannel
: 
 - IBDA_ConditionalAccessEx.CheckEntitlementToken
: 
 - IBDA_ConditionalAccessEx.CloseMmiDialog
: 
 - IBDA_ConditionalAccessEx.CreateDialogRequestNumber
: 
 - IBDA_ConditionalAccessEx.OpenBroadcastMmi
: 
 - IBDA_ConditionalAccessEx.SetCaptureToken
: 
 - IBDA_DeviceControl.CheckChanges
: 
 - IBDA_DeviceControl.CommitChanges
: 
 - IBDA_DeviceControl.GetChangeState
: 
 - IBDA_DeviceControl.StartChanges
: 
 - IBDA_DigitalDemodulator.get_InnerFECMethod
: 
 - IBDA_DigitalDemodulator.get_InnerFECRate
: 
 - IBDA_DigitalDemodulator.get_ModulationType
: 
 - IBDA_DigitalDemodulator.get_OuterFECMethod
: 
 - IBDA_DigitalDemodulator.get_OuterFECRate
: 
 - IBDA_DigitalDemodulator.get_SpectralInversion
: 
 - IBDA_DigitalDemodulator.get_SymbolRate
: 
 - IBDA_DigitalDemodulator.put_InnerFECMethod
: 
 - IBDA_DigitalDemodulator.put_InnerFECRate
: 
 - IBDA_DigitalDemodulator.put_ModulationType
: 
 - IBDA_DigitalDemodulator.put_OuterFECMethod
: 
 - IBDA_DigitalDemodulator.put_OuterFECRate
: 
 - IBDA_DigitalDemodulator.put_SpectralInversion
: 
 - IBDA_DigitalDemodulator.put_SymbolRate
: 
 - IBDA_DigitalDemodulator2.get_GuardInterval
: 
 - IBDA_DigitalDemodulator2.get_Pilot
: 
 - IBDA_DigitalDemodulator2.get_RollOff
: 
 - IBDA_DigitalDemodulator2.get_TransmissionMode
: 
 - IBDA_DigitalDemodulator2.put_GuardInterval
: 
 - IBDA_DigitalDemodulator2.put_Pilot
: 
 - IBDA_DigitalDemodulator2.put_RollOff
: 
 - IBDA_DigitalDemodulator2.put_TransmissionMode
: 
 - IBDA_DiseqCommand.get_DiseqResponse
: 
 - IBDA_DiseqCommand.put_DiseqLNBSource
: 
 - IBDA_DiseqCommand.put_DiseqRepeats
: 
 - IBDA_DiseqCommand.put_DiseqSendCommand
: 
 - IBDA_DiseqCommand.put_DiseqUseToneBurst
: 
 - IBDA_DiseqCommand.put_EnableDiseqCommands
: 
 - IBDA_DRIDRMService.GetDRMStatus
: 
 - IBDA_DRIDRMService.GetPairingStatus
: 
 - IBDA_DRIDRMService.SetDRM
: 
 - IBDA_DRM.GetDRMPairingStatus
: 
 - IBDA_DRM.PerformDRMPairing
: 
 - IBDA_DRMService.GetDRMStatus
: 
 - IBDA_DRMService.SetDRM
: 
 - IBDA_EasMessage.get_EasMessage
: 
 - IBDA_Encoder.EnumAudioCapability
: 
 - IBDA_Encoder.EnumVideoCapability
: 
 - IBDA_Encoder.GetState
: 
 - IBDA_Encoder.QueryCapabilities
: 
 - IBDA_Encoder.SetParameters
: 
 - IBDA_EthernetFilter.GetMulticastList
: 
 - IBDA_EthernetFilter.GetMulticastListSize
: 
 - IBDA_EthernetFilter.GetMulticastMode
: 
 - IBDA_EthernetFilter.PutMulticastList
: 
 - IBDA_EthernetFilter.PutMulticastMode
: 
 - IBDA_EventingService.CompleteEvent
: 
 - IBDA_FDC.AddPid
: 
 - IBDA_FDC.AddTid
: 
 - IBDA_FDC.GetStatus
: 
 - IBDA_FDC.GetTableSection
: 
 - IBDA_FDC.RemovePid
: 
 - IBDA_FDC.RemoveTid
: 
 - IBDA_FDC.RequestTables
: 
 - IBDA_FrequencyFilter.get_Autotune
: 
 - IBDA_FrequencyFilter.get_Bandwidth
: 
 - IBDA_FrequencyFilter.get_Frequency
: 
 - IBDA_FrequencyFilter.get_FrequencyMultiplier
: 
 - IBDA_FrequencyFilter.get_Polarity
: 
 - IBDA_FrequencyFilter.get_Range
: 
 - IBDA_FrequencyFilter.put_Autotune
: 
 - IBDA_FrequencyFilter.put_Bandwidth
: 
 - IBDA_FrequencyFilter.put_Frequency
: 
 - IBDA_FrequencyFilter.put_FrequencyMultiplier
: 
 - IBDA_FrequencyFilter.put_Polarity
: 
 - IBDA_FrequencyFilter.put_Range
: 
 - IBDA_GuideDataDeliveryService.GetGuideData
: 
 - IBDA_GuideDataDeliveryService.GetGuideDataType
: 
 - IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml
: 
 - IBDA_GuideDataDeliveryService.GetServices
: 
 - IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx
: 
 - IBDA_GuideDataDeliveryService.RequestGuideDataUpdate
: 
 - IBDA_IPSinkControl.GetAdapterIPAddress
: 
 - IBDA_IPSinkControl.GetMulticastList
: 
 - IBDA_IPSinkInfo.get_AdapterDescription
: 
 - IBDA_IPSinkInfo.get_AdapterIPAddress
: 
 - IBDA_IPSinkInfo.get_MulticastList
: 
 - IBDA_IPV4Filter.GetMulticastList
: 
 - IBDA_IPV4Filter.GetMulticastListSize
: 
 - IBDA_IPV4Filter.GetMulticastMode
: 
 - IBDA_IPV4Filter.PutMulticastList
: 
 - IBDA_IPV4Filter.PutMulticastMode
: 
 - IBDA_IPV6Filter.GetMulticastList
: 
 - IBDA_IPV6Filter.GetMulticastListSize
: 
 - IBDA_IPV6Filter.GetMulticastMode
: 
 - IBDA_IPV6Filter.PutMulticastList
: 
 - IBDA_IPV6Filter.PutMulticastMode
: 
 - IBDA_ISDBConditionalAccess.SetIsdbCasRequest
: 
 - IBDA_LNBInfo.get_HighLowSwitchFrequency
: 
 - IBDA_LNBInfo.get_LocalOscilatorFrequencyHighBand
: 
 - IBDA_LNBInfo.get_LocalOscilatorFrequencyLowBand
: 
 - IBDA_LNBInfo.put_HighLowSwitchFrequency
: 
 - IBDA_LNBInfo.put_LocalOscilatorFrequencyHighBand
: 
 - IBDA_LNBInfo.put_LocalOscilatorFrequencyLowBand
: 
 - IBDA_MUX.GetPidList
: 
 - IBDA_MUX.SetPidList
: 
 - IBDA_NameValueService.GetValue
: 
 - IBDA_NameValueService.GetValueNameByIndex
: 
 - IBDA_NameValueService.SetValue
: 
 - IBDA_NetworkProvider.GetNetworkType
: 
 - IBDA_NetworkProvider.GetSignalSource
: 
 - IBDA_NetworkProvider.GetTuningSpace
: 
 - IBDA_NetworkProvider.PutSignalSource
: 
 - IBDA_NetworkProvider.PutTuningSpace
: 
 - IBDA_NetworkProvider.RegisterDeviceFilter
: 
 - IBDA_NetworkProvider.UnRegisterDeviceFilter
: 
 - IBDA_NullTransform.Start
: 
 - IBDA_NullTransform.Stop
: 
 - IBDA_PinControl.GetPinID
: 
 - IBDA_PinControl.GetPinType
: 
 - IBDA_PinControl.RegistrationContext
: 
 - IBDA_SignalProperties.GetNetworkType
: 
 - IBDA_SignalProperties.GetSignalSource
: 
 - IBDA_SignalProperties.GetTuningSpace
: 
 - IBDA_SignalProperties.PutNetworkType
: 
 - IBDA_SignalProperties.PutSignalSource
: 
 - IBDA_SignalProperties.PutTuningSpace
: 
 - IBDA_SignalStatistics.get_SampleTime
: 
 - IBDA_SignalStatistics.get_SignalLocked
: 
 - IBDA_SignalStatistics.get_SignalPresent
: 
 - IBDA_SignalStatistics.get_SignalQuality
: 
 - IBDA_SignalStatistics.get_SignalStrength
: 
 - IBDA_SignalStatistics.put_SampleTime
: 
 - IBDA_SignalStatistics.put_SignalLocked
: 
 - IBDA_SignalStatistics.put_SignalPresent
: 
 - IBDA_SignalStatistics.put_SignalQuality
: 
 - IBDA_SignalStatistics.put_SignalStrength
: 
 - IBDA_Topology.CreatePin
: 
 - IBDA_Topology.CreateTopology
: 
 - IBDA_Topology.DeletePin
: 
 - IBDA_Topology.GetControlNode
: 
 - IBDA_Topology.GetNodeDescriptors
: 
 - IBDA_Topology.GetNodeInterfaces
: 
 - IBDA_Topology.GetNodeTypes
: 
 - IBDA_Topology.GetPinTypes
: 
 - IBDA_Topology.GetTemplateConnections
: 
 - IBDA_Topology.SetMediaType
: 
 - IBDA_Topology.SetMedium
: 
 - IBDA_TransportStreamInfo.get_PatTableTickCount
: 
 - IBDA_UserActivityService.GetUserActivityInterval
: 
 - IBDA_UserActivityService.SetCurrentTunerUseReason
: 
 - IBDA_UserActivityService.UserActivityDetected
: 
 - IBDA_VoidTransform.Start
: 
 - IBDA_VoidTransform.Stop
: 
 - ICCSubStreamFiltering.get_SubstreamTypes
: 
 - ICCSubStreamFiltering.put_SubstreamTypes
: 
 - IEnumPIDMap.Clone
: 
 - IEnumPIDMap.Next
: 
 - IEnumPIDMap.Reset
: 
 - IEnumPIDMap.Skip
: 
 - IFrequencyMap.get_CountryCode
: 
 - IFrequencyMap.get_CountryCodeList
: 
 - IFrequencyMap.get_DefaultFrequencyMapping
: 
 - IFrequencyMap.get_FrequencyMapping
: 
 - IFrequencyMap.put_CountryCode
: 
 - IFrequencyMap.put_FrequencyMapping
: 
 - IMPEG2PIDMap.EnumPIDMap
: 
 - IMPEG2PIDMap.MapPID
: 
 - IMPEG2PIDMap.UnmapPID
: 
 - IBDA_AutoDemodulate
: 
 - IBDA_AutoDemodulateEx
: 
 - IBDA_AUX
: 
 - IBDA_ConditionalAccess
: 
 - IBDA_ConditionalAccessEx
: 
 - IBDA_DeviceControl
: 
 - IBDA_DigitalDemodulator
: 
 - IBDA_DigitalDemodulator2
: 
 - IBDA_DiseqCommand
: 
 - IBDA_DRIDRMService
: 
 - IBDA_DRM
: 
 - IBDA_DRMService
: 
 - IBDA_EasMessage
: 
 - IBDA_Encoder
: 
 - IBDA_EthernetFilter
: 
 - IBDA_EventingService
: 
 - IBDA_FDC
: 
 - IBDA_FrequencyFilter
: 
 - IBDA_GuideDataDeliveryService
: 
 - IBDA_IPSinkControl
: 
 - IBDA_IPSinkInfo
: 
 - IBDA_IPV4Filter
: 
 - IBDA_IPV6Filter
: 
 - IBDA_ISDBConditionalAccess
: 
 - IBDA_LNBInfo
: 
 - IBDA_MUX
: 
 - IBDA_NameValueService
: 
 - IBDA_NetworkProvider
: 
 - IBDA_NullTransform
: 
 - IBDA_PinControl
: 
 - IBDA_SignalProperties
: 
 - IBDA_SignalStatistics
: 
 - IBDA_Topology
: 
 - IBDA_TransportStreamInfo
: 
 - IBDA_UserActivityService
: 
 - IBDA_VoidTransform
: 
 - ICCSubStreamFiltering
: 
 - IEnumPIDMap
: 
 - IFrequencyMap
: 
 - IMPEG2PIDMap
: 
 - EALocationCodeType
: 
 - SmartCardApplication
: 
 - bdaiface_enums.h
: 
 - bdatif.h
: 
 - IBDA_TIF_REGISTRATION.RegisterTIFEx
: 
 - IBDA_TIF_REGISTRATION.UnregisterTIF
: 
 - IEnumGuideDataProperties.Clone
: 
 - IEnumGuideDataProperties.Next
: 
 - IEnumGuideDataProperties.Reset
: 
 - IEnumGuideDataProperties.Skip
: 
 - IEnumTuneRequests.Clone
: 
 - IEnumTuneRequests.Next
: 
 - IEnumTuneRequests.Reset
: 
 - IEnumTuneRequests.Skip
: 
 - IGuideData.GetGuideProgramIDs
: 
 - IGuideData.GetProgramProperties
: 
 - IGuideData.GetScheduleEntryIDs
: 
 - IGuideData.GetScheduleEntryProperties
: 
 - IGuideData.GetServiceProperties
: 
 - IGuideData.GetServices
: 
 - IGuideDataEvent.GuideDataAcquired
: 
 - IGuideDataEvent.ProgramChanged
: 
 - IGuideDataEvent.ProgramDeleted
: 
 - IGuideDataEvent.ScheduleDeleted
: 
 - IGuideDataEvent.ScheduleEntryChanged
: 
 - IGuideDataEvent.ServiceChanged
: 
 - IGuideDataEvent.ServiceDeleted
: 
 - IGuideDataProperty.get_Language
: 
 - IGuideDataProperty.get_Name
: 
 - IGuideDataProperty.get_Value
: 
 - IMPEG2_TIF_CONTROL.AddPIDs
: 
 - IMPEG2_TIF_CONTROL.DeletePIDs
: 
 - IMPEG2_TIF_CONTROL.GetPIDCount
: 
 - IMPEG2_TIF_CONTROL.GetPIDs
: 
 - IMPEG2_TIF_CONTROL.RegisterTIF
: 
 - IMPEG2_TIF_CONTROL.UnregisterTIF
: 
 - ITuneRequestInfo.CreateComponentList
: 
 - ITuneRequestInfo.GetComponentData
: 
 - ITuneRequestInfo.GetLocatorData
: 
 - ITuneRequestInfo.GetNextLocator
: 
 - ITuneRequestInfo.GetNextProgram
: 
 - ITuneRequestInfo.GetPreviousLocator
: 
 - ITuneRequestInfo.GetPreviousProgram
: 
 - IBDA_TIF_REGISTRATION
: 
 - IEnumGuideDataProperties
: 
 - IEnumTuneRequests
: 
 - IGuideData
: 
 - IGuideDataEvent
: 
 - IGuideDataProperty
: 
 - IMPEG2_TIF_CONTROL
: 
 - ITuneRequestInfo
: 
 - bits.h
: 
 - __MIDL_IBackgroundCopyError_0001
: 
 - __MIDL_IBackgroundCopyJob_0001
: 
 - __MIDL_IBackgroundCopyJob_0002
: 
 - __MIDL_IBackgroundCopyJob_0003
: 
 - __MIDL_IBackgroundCopyJob_0004
: 
 - IBackgroundCopyCallback.JobError
: 
 - IBackgroundCopyCallback.JobModification
: 
 - IBackgroundCopyCallback.JobTransferred
: 
 - IBackgroundCopyError.GetError
: 
 - IBackgroundCopyError.GetErrorContextDescription
: 
 - IBackgroundCopyError.GetErrorDescription
: 
 - IBackgroundCopyError.GetFile
: 
 - IBackgroundCopyError.GetProtocol
: 
 - IBackgroundCopyFile.GetLocalName
: 
 - IBackgroundCopyFile.GetProgress
: 
 - IBackgroundCopyFile.GetRemoteName
: 
 - IBackgroundCopyJob.AddFile
: 
 - IBackgroundCopyJob.AddFileSet
: 
 - IBackgroundCopyJob.Cancel
: 
 - IBackgroundCopyJob.Complete
: 
 - IBackgroundCopyJob.EnumFiles
: 
 - IBackgroundCopyJob.GetDescription
: 
 - IBackgroundCopyJob.GetDisplayName
: 
 - IBackgroundCopyJob.GetError
: 
 - IBackgroundCopyJob.GetErrorCount
: 
 - IBackgroundCopyJob.GetId
: 
 - IBackgroundCopyJob.GetMinimumRetryDelay
: 
 - IBackgroundCopyJob.GetNoProgressTimeout
: 
 - IBackgroundCopyJob.GetNotifyFlags
: 
 - IBackgroundCopyJob.GetNotifyInterface
: 
 - IBackgroundCopyJob.GetOwner
: 
 - IBackgroundCopyJob.GetPriority
: 
 - IBackgroundCopyJob.GetProgress
: 
 - IBackgroundCopyJob.GetProxySettings
: 
 - IBackgroundCopyJob.GetState
: 
 - IBackgroundCopyJob.GetTimes
: 
 - IBackgroundCopyJob.GetType
: 
 - IBackgroundCopyJob.Resume
: 
 - IBackgroundCopyJob.SetDescription
: 
 - IBackgroundCopyJob.SetDisplayName
: 
 - IBackgroundCopyJob.SetMinimumRetryDelay
: 
 - IBackgroundCopyJob.SetNoProgressTimeout
: 
 - IBackgroundCopyJob.SetNotifyFlags
: 
 - IBackgroundCopyJob.SetNotifyInterface
: 
 - IBackgroundCopyJob.SetPriority
: 
 - IBackgroundCopyJob.SetProxySettings
: 
 - IBackgroundCopyJob.Suspend
: 
 - IBackgroundCopyJob.TakeOwnership
: 
 - IBackgroundCopyManager.CreateJob
: 
 - IBackgroundCopyManager.EnumJobs
: 
 - IBackgroundCopyManager.GetErrorDescription
: 
 - IBackgroundCopyManager.GetJob
: 
 - IEnumBackgroundCopyFiles.Clone
: 
 - IEnumBackgroundCopyFiles.GetCount
: 
 - IEnumBackgroundCopyFiles.Next
: 
 - IEnumBackgroundCopyFiles.Reset
: 
 - IEnumBackgroundCopyFiles.Skip
: 
 - IEnumBackgroundCopyJobs.Clone
: 
 - IEnumBackgroundCopyJobs.GetCount
: 
 - IEnumBackgroundCopyJobs.Next
: 
 - IEnumBackgroundCopyJobs.Reset
: 
 - IEnumBackgroundCopyJobs.Skip
: 
 - IBackgroundCopyCallback
: 
 - IBackgroundCopyError
: 
 - IBackgroundCopyFile
: 
 - IBackgroundCopyJob
: 
 - IBackgroundCopyManager
: 
 - IEnumBackgroundCopyFiles
: 
 - IEnumBackgroundCopyJobs
: 
 - _BG_FILE_INFO
: 
 - _BG_FILE_PROGRESS
: 
 - _BG_JOB_PROGRESS
: 
 - _BG_JOB_TIMES
: 
 - bits10_1.h
: 
 - IBackgroundCopyCallback3.FileRangesTransferred
: 
 - IBackgroundCopyFile6.GetFilledFileRanges
: 
 - IBackgroundCopyFile6.RequestFileRanges
: 
 - IBackgroundCopyFile6.UpdateDownloadPosition
: 
 - IBackgroundCopyCallback3
: 
 - IBackgroundCopyFile6
: 
 - bits1_5.h
: 
 - __MIDL_IBackgroundCopyJob2_0001
: 
 - __MIDL_IBackgroundCopyJob2_0002
: 
 - IBackgroundCopyJob2.GetNotifyCmdLine
: 
 - IBackgroundCopyJob2.GetReplyData
: 
 - IBackgroundCopyJob2.GetReplyFileName
: 
 - IBackgroundCopyJob2.GetReplyProgress
: 
 - IBackgroundCopyJob2.RemoveCredentials
: 
 - IBackgroundCopyJob2.SetCredentials
: 
 - IBackgroundCopyJob2.SetNotifyCmdLine
: 
 - IBackgroundCopyJob2.SetReplyFileName
: 
 - IBackgroundCopyJob2
: 
 - _BG_JOB_REPLY_PROGRESS
: 
 - __MIDL_IBackgroundCopyJob2_0003
: 
 - __MIDL_IBackgroundCopyJob2_0004
: 
 - __MIDL_IBackgroundCopyJob2_0005
: 
 - bits2_0.h
: 
 - IBackgroundCopyFile2.GetFileRanges
: 
 - IBackgroundCopyFile2.SetRemoteName
: 
 - IBackgroundCopyJob3.AddFileWithRanges
: 
 - IBackgroundCopyJob3.GetFileACLFlags
: 
 - IBackgroundCopyJob3.ReplaceRemotePrefix
: 
 - IBackgroundCopyJob3.SetFileACLFlags
: 
 - IBackgroundCopyFile2
: 
 - IBackgroundCopyJob3
: 
 - _BG_FILE_RANGE
: 
 - bits2_5.h
: 
 - __MIDL_IBackgroundCopyJobHttpOptions_0001
: 
 - IBackgroundCopyJobHttpOptions.GetClientCertificate
: 
 - IBackgroundCopyJobHttpOptions.GetCustomHeaders
: 
 - IBackgroundCopyJobHttpOptions.GetSecurityFlags
: 
 - IBackgroundCopyJobHttpOptions.RemoveClientCertificate
: 
 - IBackgroundCopyJobHttpOptions.SetClientCertificateByID
: 
 - IBackgroundCopyJobHttpOptions.SetClientCertificateByName
: 
 - IBackgroundCopyJobHttpOptions.SetCustomHeaders
: 
 - IBackgroundCopyJobHttpOptions.SetSecurityFlags
: 
 - IBackgroundCopyJobHttpOptions
: 
 - bits3_0.h
: 
 - IBackgroundCopyCallback2.FileTransferred
: 
 - IBackgroundCopyFile3.GetTemporaryName
: 
 - IBackgroundCopyFile3.GetValidationState
: 
 - IBackgroundCopyFile3.IsDownloadedFromPeer
: 
 - IBackgroundCopyFile3.SetValidationState
: 
 - IBackgroundCopyJob4.GetMaximumDownloadTime
: 
 - IBackgroundCopyJob4.GetOwnerElevationState
: 
 - IBackgroundCopyJob4.GetOwnerIntegrityLevel
: 
 - IBackgroundCopyJob4.GetPeerCachingFlags
: 
 - IBackgroundCopyJob4.SetMaximumDownloadTime
: 
 - IBackgroundCopyJob4.SetPeerCachingFlags
: 
 - IBitsPeer.GetPeerName
: 
 - IBitsPeer.IsAuthenticated
: 
 - IBitsPeer.IsAvailable
: 
 - IBitsPeerCacheAdministration.ClearPeers
: 
 - IBitsPeerCacheAdministration.ClearRecords
: 
 - IBitsPeerCacheAdministration.DeleteRecord
: 
 - IBitsPeerCacheAdministration.DeleteUrl
: 
 - IBitsPeerCacheAdministration.DiscoverPeers
: 
 - IBitsPeerCacheAdministration.EnumPeers
: 
 - IBitsPeerCacheAdministration.EnumRecords
: 
 - IBitsPeerCacheAdministration.GetConfigurationFlags
: 
 - IBitsPeerCacheAdministration.GetMaximumCacheSize
: 
 - IBitsPeerCacheAdministration.GetMaximumContentAge
: 
 - IBitsPeerCacheAdministration.GetRecord
: 
 - IBitsPeerCacheAdministration.SetConfigurationFlags
: 
 - IBitsPeerCacheAdministration.SetMaximumCacheSize
: 
 - IBitsPeerCacheAdministration.SetMaximumContentAge
: 
 - IBitsPeerCacheRecord.GetFileModificationTime
: 
 - IBitsPeerCacheRecord.GetFileRanges
: 
 - IBitsPeerCacheRecord.GetFileSize
: 
 - IBitsPeerCacheRecord.GetId
: 
 - IBitsPeerCacheRecord.GetLastAccessTime
: 
 - IBitsPeerCacheRecord.GetOriginUrl
: 
 - IBitsPeerCacheRecord.IsFileValidated
: 
 - IEnumBitsPeerCacheRecords.Clone
: 
 - IEnumBitsPeerCacheRecords.GetCount
: 
 - IEnumBitsPeerCacheRecords.Next
: 
 - IEnumBitsPeerCacheRecords.Reset
: 
 - IEnumBitsPeerCacheRecords.Skip
: 
 - IEnumBitsPeers.Clone
: 
 - IEnumBitsPeers.GetCount
: 
 - IEnumBitsPeers.Next
: 
 - IEnumBitsPeers.Reset
: 
 - IEnumBitsPeers.Skip
: 
 - IBackgroundCopyCallback2
: 
 - IBackgroundCopyFile3
: 
 - IBackgroundCopyJob4
: 
 - IBitsPeer
: 
 - IBitsPeerCacheAdministration
: 
 - IBitsPeerCacheRecord
: 
 - IEnumBitsPeerCacheRecords
: 
 - IEnumBitsPeers
: 
 - bits4_0.h
: 
 - IBackgroundCopyFile4.GetPeerDownloadStats
: 
 - IBitsTokenOptions.ClearHelperToken
: 
 - IBitsTokenOptions.GetHelperTokenFlags
: 
 - IBitsTokenOptions.GetHelperTokenSid
: 
 - IBitsTokenOptions.SetHelperToken
: 
 - IBitsTokenOptions.SetHelperTokenFlags
: 
 - IBackgroundCopyFile4
: 
 - IBitsTokenOptions
: 
 - bits5_0.h
: 
 - __MIDL___MIDL_itf_bits5_0_0000_0000_0001
: 
 - __MIDL___MIDL_itf_bits5_0_0000_0000_0002
: 
 - __MIDL___MIDL_itf_bits5_0_0000_0000_0004
: 
 - IBackgroundCopyFile5.GetProperty
: 
 - IBackgroundCopyFile5.SetProperty
: 
 - IBackgroundCopyJob5.GetProperty
: 
 - IBackgroundCopyJob5.SetProperty
: 
 - IBackgroundCopyFile5
: 
 - IBackgroundCopyJob5
: 
 - __MIDL___MIDL_itf_bits5_0_0000_0000_0003
: 
 - __MIDL___MIDL_itf_bits5_0_0000_0000_0005
: 
 - bitscfg.h
: 
 - IBITSExtensionSetup.DisableBITSUploads
: 
 - IBITSExtensionSetup.EnableBITSUploads
: 
 - IBITSExtensionSetup.GetCleanupTask
: 
 - IBITSExtensionSetup.GetCleanupTaskName
: 
 - IBITSExtensionSetupFactory.GetObject
: 
 - IBITSExtensionSetup
: 
 - IBITSExtensionSetupFactory
: 
 - bluetoothapis.h
: 
 - PFN_AUTHENTICATION_CALLBACK
: 
 - PFN_AUTHENTICATION_CALLBACK_EX
: 
 - PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK
: 
 - PFN_DEVICE_CALLBACK
: 
 - _BLUETOOTH_AUTHENTICATION_METHOD
: 
 - _BLUETOOTH_AUTHENTICATION_REQUIREMENTS
: 
 - _BLUETOOTH_IO_CAPABILITY
: 
 - BluetoothAuthenticateDevice
: 
 - BluetoothAuthenticateDeviceEx
: 
 - BluetoothAuthenticateMultipleDevices
: 
 - BluetoothDisplayDeviceProperties
: 
 - BluetoothEnableDiscovery
: 
 - BluetoothEnableIncomingConnections
: 
 - BluetoothEnumerateInstalledServices
: 
 - BluetoothFindDeviceClose
: 
 - BluetoothFindFirstDevice
: 
 - BluetoothFindFirstRadio
: 
 - BluetoothFindNextDevice
: 
 - BluetoothFindNextRadio
: 
 - BluetoothFindRadioClose
: 
 - BluetoothGetDeviceInfo
: 
 - BluetoothGetRadioInfo
: 
 - BluetoothIsConnectable
: 
 - BluetoothIsDiscoverable
: 
 - BluetoothIsVersionAvailable
: 
 - BluetoothRegisterForAuthentication
: 
 - BluetoothRegisterForAuthenticationEx
: 
 - BluetoothRemoveDevice
: 
 - BluetoothSdpEnumAttributes
: 
 - BluetoothSdpGetAttributeValue
: 
 - BluetoothSdpGetContainerElementData
: 
 - BluetoothSdpGetElementData
: 
 - BluetoothSdpGetString
: 
 - BluetoothSelectDevices
: 
 - BluetoothSelectDevicesFree
: 
 - BluetoothSendAuthenticationResponse
: 
 - BluetoothSendAuthenticationResponseEx
: 
 - BluetoothSetLocalServiceInfo
: 
 - BluetoothSetServiceState
: 
 - BluetoothUnregisterAuthentication
: 
 - BluetoothUpdateDeviceRecord
: 
 - _BLUETOOTH_ADDRESS
: 
 - _BLUETOOTH_AUTHENTICATE_RESPONSE
: 
 - _BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
: 
 - _BLUETOOTH_COD_PAIRS
: 
 - _BLUETOOTH_DEVICE_INFO
: 
 - _BLUETOOTH_DEVICE_SEARCH_PARAMS
: 
 - _BLUETOOTH_FIND_RADIO_PARAMS
: 
 - _BLUETOOTH_LOCAL_SERVICE_INFO
: 
 - _BLUETOOTH_NUMERIC_COMPARISON_INFO
: 
 - _BLUETOOTH_OOB_DATA_INFO
: 
 - _BLUETOOTH_PASSKEY_INFO
: 
 - _BLUETOOTH_PIN_INFO
: 
 - _BLUETOOTH_RADIO_INFO
: 
 - _BLUETOOTH_SELECT_DEVICE_PARAMS
: 
 - _SDP_ELEMENT_DATA
: 
 - _SDP_STRING_TYPE_DATA
: 
 - BluetoothGATTAbortReliableWrite
: 
 - BluetoothGATTBeginReliableWrite
: 
 - BluetoothGATTEndReliableWrite
: 
 - BluetoothGATTGetCharacteristics
: 
 - BluetoothGATTGetCharacteristicValue
: 
 - BluetoothGATTGetDescriptors
: 
 - BluetoothGATTGetDescriptorValue
: 
 - BluetoothGATTGetIncludedServices
: 
 - BluetoothGATTGetServices
: 
 - BluetoothGATTRegisterEvent
: 
 - BluetoothGATTSetCharacteristicValue
: 
 - BluetoothGATTSetDescriptorValue
: 
 - BluetoothGATTUnregisterEvent
: 
 - bthdef.h
: 
 - _BTH_DEVICE_INFO
: 
 - _BTH_HCI_EVENT_INFO
: 
 - _BTH_L2CAP_EVENT_INFO
: 
 - _BTH_RADIO_IN_RANGE
: 
 - bthledef.h
: 
 - PFNBLUETOOTH_GATT_EVENT_CALLBACK
: 
 - _BTH_LE_GATT_DESCRIPTOR_TYPE
: 
 - _BTH_LE_GATT_EVENT_TYPE
: 
 - _BLUETOOTH_GATT_VALUE_CHANGED_EVENT
: 
 - _BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
: 
 - _BTH_LE_GATT_CHARACTERISTIC
: 
 - _BTH_LE_GATT_CHARACTERISTIC_VALUE
: 
 - _BTH_LE_GATT_DESCRIPTOR
: 
 - _BTH_LE_GATT_DESCRIPTOR_VALUE
: 
 - _BTH_LE_GATT_SERVICE
: 
 - _BTH_LE_UUID
: 
 - bthsdpdef.h
: 
 - SdpQueryUuidUnion
: 
 - _SdpAttributeRange
: 
 - _SdpQueryUuid
: 
 - callobj.h
: 
 - CALLFRAME_FREE
: 
 - CALLFRAME_NULL
: 
 - CALLFRAME_WALK
: 
 - __MIDL_ICallFrame_0003
: 
 - CoGetInterceptor
: 
 - ICallFrame.Copy
: 
 - ICallFrame.Free
: 
 - ICallFrame.FreeParam
: 
 - ICallFrame.GetIIDAndMethod
: 
 - ICallFrame.GetInfo
: 
 - ICallFrame.GetMarshalSizeMax
: 
 - ICallFrame.GetNames
: 
 - ICallFrame.GetParam
: 
 - ICallFrame.GetParamInfo
: 
 - ICallFrame.GetReturnValue
: 
 - ICallFrame.GetStackLocation
: 
 - ICallFrame.Invoke
: 
 - ICallFrame.Marshal
: 
 - ICallFrame.ReleaseMarshalData
: 
 - ICallFrame.SetParam
: 
 - ICallFrame.SetReturnValue
: 
 - ICallFrame.SetStackLocation
: 
 - ICallFrame.Unmarshal
: 
 - ICallFrame.WalkFrame
: 
 - ICallFrameEvents.OnCall
: 
 - ICallFrameWalker.OnWalkInterface
: 
 - ICallIndirect.CallIndirect
: 
 - ICallIndirect.GetIID
: 
 - ICallIndirect.GetMethodInfo
: 
 - ICallIndirect.GetStackSize
: 
 - ICallInterceptor.GetRegisteredSink
: 
 - ICallInterceptor.RegisterSink
: 
 - ICallUnmarshal.ReleaseMarshalData
: 
 - ICallUnmarshal.Unmarshal
: 
 - ICallFrame
: 
 - ICallFrameEvents
: 
 - ICallFrameWalker
: 
 - ICallIndirect
: 
 - ICallInterceptor
: 
 - ICallUnmarshal
: 
 - __MIDL_ICallFrame_0001
: 
 - __MIDL_ICallFrame_0002
: 
 - __MIDL_ICallFrame_0004
: 
 - camerauicontrol.h
: 
 - ICameraUIControl.Close
: 
 - ICameraUIControl.GetActiveItem
: 
 - ICameraUIControl.GetCurrentViewType
: 
 - ICameraUIControl.GetSelectedItems
: 
 - ICameraUIControl.RemoveCapturedItem
: 
 - ICameraUIControl.Resume
: 
 - ICameraUIControl.Show
: 
 - ICameraUIControl.Suspend
: 
 - ICameraUIControlEventCallback.OnItemCaptured
: 
 - ICameraUIControlEventCallback.OnStartupComplete
: 
 - ICameraUIControlEventCallback.OnSuspendComplete
: 
 - ICameraUIControl
: 
 - ICameraUIControlEventCallback
: 
 - capi.h
: 
 - _JAVA_TRUST
: 
 - casetup.h
: 
 - __MIDL___MIDL_itf_casetup_0000_0002_0001
: 
 - __MIDL___MIDL_itf_casetup_0000_0003_0001
: 
 - __MIDL___MIDL_itf_casetup_0000_0004_0001
: 
 - __MIDL___MIDL_itf_casetup_0000_0005_0001
: 
 - ICertificateEnrollmentPolicyServerSetup.GetProperty
: 
 - ICertificateEnrollmentPolicyServerSetup.get_ErrorString
: 
 - ICertificateEnrollmentPolicyServerSetup.InitializeInstallDefaults
: 
 - ICertificateEnrollmentPolicyServerSetup.Install
: 
 - ICertificateEnrollmentPolicyServerSetup.SetProperty
: 
 - ICertificateEnrollmentPolicyServerSetup.UnInstall
: 
 - ICertificateEnrollmentServerSetup.GetProperty
: 
 - ICertificateEnrollmentServerSetup.get_ErrorString
: 
 - ICertificateEnrollmentServerSetup.InitializeInstallDefaults
: 
 - ICertificateEnrollmentServerSetup.Install
: 
 - ICertificateEnrollmentServerSetup.SetApplicationPoolCredentials
: 
 - ICertificateEnrollmentServerSetup.SetProperty
: 
 - ICertificateEnrollmentServerSetup.UnInstall
: 
 - ICertSrvSetup.CAImportPFX
: 
 - ICertSrvSetup.GetCASetupProperty
: 
 - ICertSrvSetup.GetExistingCACertificates
: 
 - ICertSrvSetup.GetHashAlgorithmList
: 
 - ICertSrvSetup.GetKeyLengthList
: 
 - ICertSrvSetup.GetPrivateKeyContainerList
: 
 - ICertSrvSetup.GetProviderNameList
: 
 - ICertSrvSetup.GetSupportedCATypes
: 
 - ICertSrvSetup.get_CAErrorId
: 
 - ICertSrvSetup.get_CAErrorString
: 
 - ICertSrvSetup.InitializeDefaults
: 
 - ICertSrvSetup.Install
: 
 - ICertSrvSetup.IsPropertyEditable
: 
 - ICertSrvSetup.PostUnInstall
: 
 - ICertSrvSetup.PreUnInstall
: 
 - ICertSrvSetup.SetCADistinguishedName
: 
 - ICertSrvSetup.SetCASetupProperty
: 
 - ICertSrvSetup.SetDatabaseInformation
: 
 - ICertSrvSetup.SetParentCAInformation
: 
 - ICertSrvSetup.SetWebCAInformation
: 
 - ICertSrvSetupKeyInformation.get_ContainerName
: 
 - ICertSrvSetupKeyInformation.get_Existing
: 
 - ICertSrvSetupKeyInformation.get_ExistingCACertificate
: 
 - ICertSrvSetupKeyInformation.get_HashAlgorithm
: 
 - ICertSrvSetupKeyInformation.get_Length
: 
 - ICertSrvSetupKeyInformation.get_ProviderName
: 
 - ICertSrvSetupKeyInformation.put_ContainerName
: 
 - ICertSrvSetupKeyInformation.put_Existing
: 
 - ICertSrvSetupKeyInformation.put_ExistingCACertificate
: 
 - ICertSrvSetupKeyInformation.put_HashAlgorithm
: 
 - ICertSrvSetupKeyInformation.put_Length
: 
 - ICertSrvSetupKeyInformation.put_ProviderName
: 
 - ICertSrvSetupKeyInformationCollection.Add
: 
 - ICertSrvSetupKeyInformationCollection.get_Count
: 
 - ICertSrvSetupKeyInformationCollection.get_Item
: 
 - ICertSrvSetupKeyInformationCollection.get__NewEnum
: 
 - IMSCEPSetup.GetKeyLengthList
: 
 - IMSCEPSetup.GetMSCEPSetupProperty
: 
 - IMSCEPSetup.GetProviderNameList
: 
 - IMSCEPSetup.get_MSCEPErrorId
: 
 - IMSCEPSetup.get_MSCEPErrorString
: 
 - IMSCEPSetup.InitializeDefaults
: 
 - IMSCEPSetup.Install
: 
 - IMSCEPSetup.IsMSCEPStoreEmpty
: 
 - IMSCEPSetup.PostUnInstall
: 
 - IMSCEPSetup.PreUnInstall
: 
 - IMSCEPSetup.SetAccountInformation
: 
 - IMSCEPSetup.SetMSCEPSetupProperty
: 
 - ICertificateEnrollmentPolicyServerSetup
: 
 - ICertificateEnrollmentServerSetup
: 
 - ICertSrvSetup
: 
 - ICertSrvSetupKeyInformation
: 
 - ICertSrvSetupKeyInformationCollection
: 
 - IMSCEPSetup
: 
 - cchannel.h
: 
 - CHANNEL_INIT_EVENT_FN
: 
 - CHANNEL_OPEN_EVENT_FN
: 
 - VIRTUALCHANNELCLOSE
: 
 - VIRTUALCHANNELENTRY
: 
 - VIRTUALCHANNELINIT
: 
 - VIRTUALCHANNELOPEN
: 
 - VIRTUALCHANNELWRITE
: 
 - tagCHANNEL_ENTRY_POINTS
: 
 - celib.h
: 
 - ENUM_PERIOD
: 
 - certadm.h
: 
 - ICertAdmin.DenyRequest
: 
 - ICertAdmin.GetCRL
: 
 - ICertAdmin.GetRevocationReason
: 
 - ICertAdmin.ImportCertificate
: 
 - ICertAdmin.IsValidCertificate
: 
 - ICertAdmin.PublishCRL
: 
 - ICertAdmin.ResubmitRequest
: 
 - ICertAdmin.RevokeCertificate
: 
 - ICertAdmin.SetCertificateExtension
: 
 - ICertAdmin.SetRequestAttributes
: 
 - ICertAdmin2.DeleteRow
: 
 - ICertAdmin2.GetArchivedKey
: 
 - ICertAdmin2.GetCAProperty
: 
 - ICertAdmin2.GetCAPropertyDisplayName
: 
 - ICertAdmin2.GetCAPropertyFlags
: 
 - ICertAdmin2.GetConfigEntry
: 
 - ICertAdmin2.GetMyRoles
: 
 - ICertAdmin2.ImportKey
: 
 - ICertAdmin2.PublishCRLs
: 
 - ICertAdmin2.SetCAProperty
: 
 - ICertAdmin2.SetConfigEntry
: 
 - IOCSPAdmin.GetConfiguration
: 
 - IOCSPAdmin.GetHashAlgorithms
: 
 - IOCSPAdmin.GetMyRoles
: 
 - IOCSPAdmin.GetSecurity
: 
 - IOCSPAdmin.GetSigningCertificates
: 
 - IOCSPAdmin.get_OCSPCAConfigurationCollection
: 
 - IOCSPAdmin.get_OCSPServiceProperties
: 
 - IOCSPAdmin.Ping
: 
 - IOCSPAdmin.SetConfiguration
: 
 - IOCSPAdmin.SetSecurity
: 
 - IOCSPCAConfiguration.get_CACertificate
: 
 - IOCSPCAConfiguration.get_CAConfig
: 
 - IOCSPCAConfiguration.get_CSPName
: 
 - IOCSPCAConfiguration.get_ErrorCode
: 
 - IOCSPCAConfiguration.get_HashAlgorithm
: 
 - IOCSPCAConfiguration.get_Identifier
: 
 - IOCSPCAConfiguration.get_KeySpec
: 
 - IOCSPCAConfiguration.get_LocalRevocationInformation
: 
 - IOCSPCAConfiguration.get_Modified
: 
 - IOCSPCAConfiguration.get_ProviderCLSID
: 
 - IOCSPCAConfiguration.get_ProviderProperties
: 
 - IOCSPCAConfiguration.get_ReminderDuration
: 
 - IOCSPCAConfiguration.get_SigningCertificate
: 
 - IOCSPCAConfiguration.get_SigningCertificateTemplate
: 
 - IOCSPCAConfiguration.get_SigningFlags
: 
 - IOCSPCAConfiguration.put_CAConfig
: 
 - IOCSPCAConfiguration.put_HashAlgorithm
: 
 - IOCSPCAConfiguration.put_LocalRevocationInformation
: 
 - IOCSPCAConfiguration.put_ProviderCLSID
: 
 - IOCSPCAConfiguration.put_ProviderProperties
: 
 - IOCSPCAConfiguration.put_ReminderDuration
: 
 - IOCSPCAConfiguration.put_SigningCertificate
: 
 - IOCSPCAConfiguration.put_SigningCertificateTemplate
: 
 - IOCSPCAConfiguration.put_SigningFlags
: 
 - IOCSPCAConfigurationCollection.CreateCAConfiguration
: 
 - IOCSPCAConfigurationCollection.DeleteCAConfiguration
: 
 - IOCSPCAConfigurationCollection.get_Count
: 
 - IOCSPCAConfigurationCollection.get_Item
: 
 - IOCSPCAConfigurationCollection.get_ItemByName
: 
 - IOCSPCAConfigurationCollection.get__NewEnum
: 
 - IOCSPProperty.get_Modified
: 
 - IOCSPProperty.get_Name
: 
 - IOCSPProperty.get_Value
: 
 - IOCSPProperty.put_Value
: 
 - IOCSPPropertyCollection.CreateProperty
: 
 - IOCSPPropertyCollection.DeleteProperty
: 
 - IOCSPPropertyCollection.GetAllProperties
: 
 - IOCSPPropertyCollection.get_Count
: 
 - IOCSPPropertyCollection.get_Item
: 
 - IOCSPPropertyCollection.get_ItemByName
: 
 - IOCSPPropertyCollection.get__NewEnum
: 
 - IOCSPPropertyCollection.InitializeFromProperties
: 
 - ICertAdmin
: 
 - ICertAdmin2
: 
 - IOCSPAdmin
: 
 - IOCSPCAConfiguration
: 
 - IOCSPCAConfigurationCollection
: 
 - IOCSPProperty
: 
 - IOCSPPropertyCollection
: 
 - CertSrvBackupClose
: 
 - CertSrvBackupEnd
: 
 - CertSrvBackupFree
: 
 - CertSrvBackupGetBackupLogsW
: 
 - CertSrvBackupGetDatabaseNamesW
: 
 - CertSrvBackupGetDynamicFileListW
: 
 - CertSrvBackupOpenFileW
: 
 - CertSrvBackupPrepareW
: 
 - CertSrvBackupRead
: 
 - CertSrvBackupTruncateLogs
: 
 - CertSrvIsServerOnlineW
: 
 - CertSrvRestoreEnd
: 
 - CertSrvRestoreGetDatabaseLocationsW
: 
 - CertSrvRestorePrepareW
: 
 - CertSrvRestoreRegisterComplete
: 
 - CertSrvRestoreRegisterThroughFile
: 
 - CertSrvRestoreRegisterW
: 
 - CertSrvServerControlW
: 
 - certcli.h
: 
 - X509EnrollmentAuthFlags
: 
 - ICertConfig.GetConfig
: 
 - ICertConfig.GetField
: 
 - ICertConfig.Next
: 
 - ICertConfig.Reset
: 
 - ICertConfig2.SetSharedFolder
: 
 - ICertGetConfig.GetConfig
: 
 - ICertRequest.GetCACertificate
: 
 - ICertRequest.GetCertificate
: 
 - ICertRequest.GetDispositionMessage
: 
 - ICertRequest.GetLastStatus
: 
 - ICertRequest.GetRequestId
: 
 - ICertRequest.RetrievePending
: 
 - ICertRequest.Submit
: 
 - ICertRequest2.GetCAProperty
: 
 - ICertRequest2.GetCAPropertyDisplayName
: 
 - ICertRequest2.GetCAPropertyFlags
: 
 - ICertRequest2.GetErrorMessageText
: 
 - ICertRequest2.GetFullResponseProperty
: 
 - ICertRequest2.GetIssuedCertificate
: 
 - ICertRequest3.GetIssuedCertificate2
: 
 - ICertRequest3.GetRefreshPolicy
: 
 - ICertRequest3.GetRequestIdString
: 
 - ICertRequest3.SetCredential
: 
 - ICertConfig
: 
 - ICertConfig2
: 
 - ICertGetConfig
: 
 - ICertRequest
: 
 - ICertRequest2
: 
 - ICertRequest3
: 
 - certenc.h
: 
 - ICertEncodeAltName.Decode
: 
 - ICertEncodeAltName.Encode
: 
 - ICertEncodeAltName.GetName
: 
 - ICertEncodeAltName.GetNameChoice
: 
 - ICertEncodeAltName.GetNameCount
: 
 - ICertEncodeAltName.Reset
: 
 - ICertEncodeAltName.SetNameEntry
: 
 - ICertEncodeBitString.Decode
: 
 - ICertEncodeBitString.Encode
: 
 - ICertEncodeBitString.GetBitCount
: 
 - ICertEncodeBitString.GetBitString
: 
 - ICertEncodeCRLDistInfo.Decode
: 
 - ICertEncodeCRLDistInfo.Encode
: 
 - ICertEncodeCRLDistInfo.GetDistPointCount
: 
 - ICertEncodeCRLDistInfo.GetName
: 
 - ICertEncodeCRLDistInfo.GetNameChoice
: 
 - ICertEncodeCRLDistInfo.GetNameCount
: 
 - ICertEncodeCRLDistInfo.Reset
: 
 - ICertEncodeCRLDistInfo.SetNameCount
: 
 - ICertEncodeCRLDistInfo.SetNameEntry
: 
 - ICertEncodeDateArray.Decode
: 
 - ICertEncodeDateArray.Encode
: 
 - ICertEncodeDateArray.GetCount
: 
 - ICertEncodeDateArray.GetValue
: 
 - ICertEncodeDateArray.Reset
: 
 - ICertEncodeDateArray.SetValue
: 
 - ICertEncodeLongArray.Decode
: 
 - ICertEncodeLongArray.Encode
: 
 - ICertEncodeLongArray.GetCount
: 
 - ICertEncodeLongArray.GetValue
: 
 - ICertEncodeLongArray.Reset
: 
 - ICertEncodeLongArray.SetValue
: 
 - ICertEncodeStringArray.Decode
: 
 - ICertEncodeStringArray.Encode
: 
 - ICertEncodeStringArray.GetCount
: 
 - ICertEncodeStringArray.GetStringType
: 
 - ICertEncodeStringArray.GetValue
: 
 - ICertEncodeStringArray.Reset
: 
 - ICertEncodeStringArray.SetValue
: 
 - ICertEncodeAltName
: 
 - ICertEncodeBitString
: 
 - ICertEncodeCRLDistInfo
: 
 - ICertEncodeDateArray
: 
 - ICertEncodeLongArray
: 
 - ICertEncodeStringArray
: 
 - certenroll.h
: 
 - AlgorithmFlags
: 
 - AlgorithmOperationFlags
: 
 - AlgorithmType
: 
 - AlternativeNameType
: 
 - CERTENROLL_OBJECTID
: 
 - CERTENROLL_PROPERTYID
: 
 - CommitTemplateFlags
: 
 - EncodingType
: 
 - EnrollmentCAProperty
: 
 - EnrollmentDisplayStatus
: 
 - EnrollmentEnrollStatus
: 
 - EnrollmentPolicyFlags
: 
 - EnrollmentPolicyServerPropertyFlags
: 
 - EnrollmentSelectionStatus
: 
 - EnrollmentTemplateProperty
: 
 - InnerRequestLevel
: 
 - InstallResponseRestrictionFlags
: 
 - KeyIdentifierHashAlgorithm
: 
 - ObjectIdGroupId
: 
 - ObjectIdPublicKeyFlags
: 
 - PFXExportOptions
: 
 - Pkcs10AllowedSignatureTypes
: 
 - PolicyQualifierType
: 
 - PolicyServerUrlFlags
: 
 - PolicyServerUrlPropertyID
: 
 - RequestClientInfoClientId
: 
 - WebEnrollmentFlags
: 
 - WebSecurityLevel
: 
 - X500NameFlags
: 
 - X509CertificateEnrollmentContext
: 
 - X509CertificateTemplateEnrollmentFlag
: 
 - X509CertificateTemplateGeneralFlag
: 
 - X509CertificateTemplatePrivateKeyFlag
: 
 - X509CertificateTemplateSubjectNameFlag
: 
 - X509EnrollmentPolicyExportFlags
: 
 - X509EnrollmentPolicyLoadOption
: 
 - X509KeySpec
: 
 - X509KeyUsageFlags
: 
 - X509PrivateKeyExportFlags
: 
 - X509PrivateKeyProtection
: 
 - X509PrivateKeyUsageFlags
: 
 - X509PrivateKeyVerify
: 
 - X509ProviderType
: 
 - X509RequestInheritOptions
: 
 - X509RequestType
: 
 - IAlternativeName.get_ObjectId
: 
 - IAlternativeName.get_RawData
: 
 - IAlternativeName.get_StrValue
: 
 - IAlternativeName.get_Type
: 
 - IAlternativeName.InitializeFromOtherName
: 
 - IAlternativeName.InitializeFromRawData
: 
 - IAlternativeName.InitializeFromString
: 
 - IAlternativeNames.Add
: 
 - IAlternativeNames.Clear
: 
 - IAlternativeNames.get_Count
: 
 - IAlternativeNames.get_ItemByIndex
: 
 - IAlternativeNames.get__NewEnum
: 
 - IAlternativeNames.Remove
: 
 - IBinaryConverter.StringToString
: 
 - IBinaryConverter.StringToVariantByteArray
: 
 - IBinaryConverter.VariantByteArrayToString
: 
 - ICertificateAttestationChallenge.DecryptChallenge
: 
 - ICertificateAttestationChallenge.get_RequestID
: 
 - ICertificateAttestationChallenge.Initialize
: 
 - ICertificatePolicies.Add
: 
 - ICertificatePolicies.Clear
: 
 - ICertificatePolicies.get_Count
: 
 - ICertificatePolicies.get_ItemByIndex
: 
 - ICertificatePolicies.get__NewEnum
: 
 - ICertificatePolicies.Remove
: 
 - ICertificatePolicy.get_ObjectId
: 
 - ICertificatePolicy.get_PolicyQualifiers
: 
 - ICertificatePolicy.Initialize
: 
 - ICertificationAuthorities.Add
: 
 - ICertificationAuthorities.Clear
: 
 - ICertificationAuthorities.ComputeSiteCosts
: 
 - ICertificationAuthorities.get_Count
: 
 - ICertificationAuthorities.get_ItemByIndex
: 
 - ICertificationAuthorities.get_ItemByName
: 
 - ICertificationAuthorities.get__NewEnum
: 
 - ICertificationAuthorities.Remove
: 
 - ICertificationAuthority.get_Property
: 
 - ICertProperties.Add
: 
 - ICertProperties.Clear
: 
 - ICertProperties.get_Count
: 
 - ICertProperties.get_ItemByIndex
: 
 - ICertProperties.get__NewEnum
: 
 - ICertProperties.InitializeFromCertificate
: 
 - ICertProperties.Remove
: 
 - ICertProperty.get_PropertyId
: 
 - ICertProperty.get_RawData
: 
 - ICertProperty.InitializeDecode
: 
 - ICertProperty.InitializeFromCertificate
: 
 - ICertProperty.put_PropertyId
: 
 - ICertProperty.RemoveFromCertificate
: 
 - ICertProperty.SetValueOnCertificate
: 
 - ICertPropertyArchived.get_Archived
: 
 - ICertPropertyArchived.Initialize
: 
 - ICertPropertyArchivedKeyHash.get_ArchivedKeyHash
: 
 - ICertPropertyArchivedKeyHash.Initialize
: 
 - ICertPropertyAutoEnroll.get_TemplateName
: 
 - ICertPropertyAutoEnroll.Initialize
: 
 - ICertPropertyBackedUp.get_BackedUpTime
: 
 - ICertPropertyBackedUp.get_BackedUpValue
: 
 - ICertPropertyBackedUp.Initialize
: 
 - ICertPropertyBackedUp.InitializeFromCurrentTime
: 
 - ICertPropertyDescription.get_Description
: 
 - ICertPropertyDescription.Initialize
: 
 - ICertPropertyEnrollment.get_CADnsName
: 
 - ICertPropertyEnrollment.get_CAName
: 
 - ICertPropertyEnrollment.get_FriendlyName
: 
 - ICertPropertyEnrollment.get_RequestId
: 
 - ICertPropertyEnrollment.Initialize
: 
 - ICertPropertyEnrollmentPolicyServer.GetAuthentication
: 
 - ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerAuthentication
: 
 - ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerUrl
: 
 - ICertPropertyEnrollmentPolicyServer.GetPolicyServerId
: 
 - ICertPropertyEnrollmentPolicyServer.GetPolicyServerUrl
: 
 - ICertPropertyEnrollmentPolicyServer.GetPropertyFlags
: 
 - ICertPropertyEnrollmentPolicyServer.GetRequestIdString
: 
 - ICertPropertyEnrollmentPolicyServer.GetUrlFlags
: 
 - ICertPropertyEnrollmentPolicyServer.Initialize
: 
 - ICertPropertyFriendlyName.get_FriendlyName
: 
 - ICertPropertyFriendlyName.Initialize
: 
 - ICertPropertyKeyProvInfo.get_PrivateKey
: 
 - ICertPropertyKeyProvInfo.Initialize
: 
 - ICertPropertyRenewal.get_Renewal
: 
 - ICertPropertyRenewal.Initialize
: 
 - ICertPropertyRenewal.InitializeFromCertificateHash
: 
 - ICertPropertyRequestOriginator.get_RequestOriginator
: 
 - ICertPropertyRequestOriginator.Initialize
: 
 - ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator
: 
 - ICertPropertySHA1Hash.get_SHA1Hash
: 
 - ICertPropertySHA1Hash.Initialize
: 
 - ICryptAttribute.get_ObjectId
: 
 - ICryptAttribute.get_Values
: 
 - ICryptAttribute.InitializeFromObjectId
: 
 - ICryptAttribute.InitializeFromValues
: 
 - ICryptAttributes.Add
: 
 - ICryptAttributes.AddRange
: 
 - ICryptAttributes.Clear
: 
 - ICryptAttributes.get_Count
: 
 - ICryptAttributes.get_IndexByObjectId
: 
 - ICryptAttributes.get_ItemByIndex
: 
 - ICryptAttributes.get__NewEnum
: 
 - ICryptAttributes.Remove
: 
 - ICspAlgorithm.GetAlgorithmOid
: 
 - ICspAlgorithm.get_DefaultLength
: 
 - ICspAlgorithm.get_IncrementLength
: 
 - ICspAlgorithm.get_LongName
: 
 - ICspAlgorithm.get_MaxLength
: 
 - ICspAlgorithm.get_MinLength
: 
 - ICspAlgorithm.get_Name
: 
 - ICspAlgorithm.get_Operations
: 
 - ICspAlgorithm.get_Type
: 
 - ICspAlgorithm.get_Valid
: 
 - ICspAlgorithms.Add
: 
 - ICspAlgorithms.Clear
: 
 - ICspAlgorithms.get_Count
: 
 - ICspAlgorithms.get_IndexByObjectId
: 
 - ICspAlgorithms.get_ItemByIndex
: 
 - ICspAlgorithms.get_ItemByName
: 
 - ICspAlgorithms.get__NewEnum
: 
 - ICspAlgorithms.Remove
: 
 - ICspInformation.GetCspStatusFromOperations
: 
 - ICspInformation.GetDefaultSecurityDescriptor
: 
 - ICspInformation.get_CspAlgorithms
: 
 - ICspInformation.get_HasHardwareRandomNumberGenerator
: 
 - ICspInformation.get_IsHardwareDevice
: 
 - ICspInformation.get_IsRemovable
: 
 - ICspInformation.get_IsSmartCard
: 
 - ICspInformation.get_IsSoftwareDevice
: 
 - ICspInformation.get_KeySpec
: 
 - ICspInformation.get_LegacyCsp
: 
 - ICspInformation.get_MaxKeyContainerNameLength
: 
 - ICspInformation.get_Name
: 
 - ICspInformation.get_Type
: 
 - ICspInformation.get_Valid
: 
 - ICspInformation.get_Version
: 
 - ICspInformation.InitializeFromName
: 
 - ICspInformation.InitializeFromType
: 
 - ICspInformations.Add
: 
 - ICspInformations.AddAvailableCsps
: 
 - ICspInformations.Clear
: 
 - ICspInformations.GetCspStatusesFromOperations
: 
 - ICspInformations.GetCspStatusFromProviderName
: 
 - ICspInformations.GetEncryptionCspAlgorithms
: 
 - ICspInformations.GetHashAlgorithms
: 
 - ICspInformations.get_Count
: 
 - ICspInformations.get_ItemByIndex
: 
 - ICspInformations.get_ItemByName
: 
 - ICspInformations.get__NewEnum
: 
 - ICspInformations.Remove
: 
 - ICspStatus.get_CspAlgorithm
: 
 - ICspStatus.get_CspInformation
: 
 - ICspStatus.get_DisplayName
: 
 - ICspStatus.get_EnrollmentStatus
: 
 - ICspStatus.get_Ordinal
: 
 - ICspStatus.Initialize
: 
 - ICspStatus.put_Ordinal
: 
 - ICspStatuses.Add
: 
 - ICspStatuses.Clear
: 
 - ICspStatuses.get_Count
: 
 - ICspStatuses.get_ItemByIndex
: 
 - ICspStatuses.get_ItemByName
: 
 - ICspStatuses.get_ItemByOperations
: 
 - ICspStatuses.get_ItemByOrdinal
: 
 - ICspStatuses.get_ItemByProvider
: 
 - ICspStatuses.get__NewEnum
: 
 - ICspStatuses.Remove
: 
 - IObjectId.GetAlgorithmName
: 
 - IObjectId.get_FriendlyName
: 
 - IObjectId.get_Name
: 
 - IObjectId.get_Value
: 
 - IObjectId.InitializeFromAlgorithmName
: 
 - IObjectId.InitializeFromName
: 
 - IObjectId.InitializeFromValue
: 
 - IObjectId.put_FriendlyName
: 
 - IObjectIds.Add
: 
 - IObjectIds.AddRange
: 
 - IObjectIds.Clear
: 
 - IObjectIds.get_Count
: 
 - IObjectIds.get_ItemByIndex
: 
 - IObjectIds.get__NewEnum
: 
 - IObjectIds.Remove
: 
 - IPolicyQualifier.get_ObjectId
: 
 - IPolicyQualifier.get_Qualifier
: 
 - IPolicyQualifier.get_RawData
: 
 - IPolicyQualifier.get_Type
: 
 - IPolicyQualifier.InitializeEncode
: 
 - IPolicyQualifiers.Add
: 
 - IPolicyQualifiers.Clear
: 
 - IPolicyQualifiers.get_Count
: 
 - IPolicyQualifiers.get_ItemByIndex
: 
 - IPolicyQualifiers.get__NewEnum
: 
 - IPolicyQualifiers.Remove
: 
 - ISignerCertificate.get_Certificate
: 
 - ISignerCertificate.get_ParentWindow
: 
 - ISignerCertificate.get_PrivateKey
: 
 - ISignerCertificate.get_SignatureInformation
: 
 - ISignerCertificate.get_Silent
: 
 - ISignerCertificate.get_UIContextMessage
: 
 - ISignerCertificate.Initialize
: 
 - ISignerCertificate.put_ParentWindow
: 
 - ISignerCertificate.put_Pin
: 
 - ISignerCertificate.put_Silent
: 
 - ISignerCertificate.put_UIContextMessage
: 
 - ISignerCertificates.Add
: 
 - ISignerCertificates.Clear
: 
 - ISignerCertificates.Find
: 
 - ISignerCertificates.get_Count
: 
 - ISignerCertificates.get_ItemByIndex
: 
 - ISignerCertificates.get__NewEnum
: 
 - ISignerCertificates.Remove
: 
 - ISmimeCapabilities.Add
: 
 - ISmimeCapabilities.AddAvailableSmimeCapabilities
: 
 - ISmimeCapabilities.AddFromCsp
: 
 - ISmimeCapabilities.Clear
: 
 - ISmimeCapabilities.get_Count
: 
 - ISmimeCapabilities.get_ItemByIndex
: 
 - ISmimeCapabilities.get__NewEnum
: 
 - ISmimeCapabilities.Remove
: 
 - ISmimeCapability.get_BitCount
: 
 - ISmimeCapability.get_ObjectId
: 
 - ISmimeCapability.Initialize
: 
 - IX500DistinguishedName.Decode
: 
 - IX500DistinguishedName.Encode
: 
 - IX500DistinguishedName.get_EncodedName
: 
 - IX500DistinguishedName.get_Name
: 
 - IX509Attribute.get_ObjectId
: 
 - IX509Attribute.get_RawData
: 
 - IX509Attribute.Initialize
: 
 - IX509AttributeArchiveKey.get_EncryptedKeyBlob
: 
 - IX509AttributeArchiveKey.get_EncryptionAlgorithm
: 
 - IX509AttributeArchiveKey.get_EncryptionStrength
: 
 - IX509AttributeArchiveKey.InitializeDecode
: 
 - IX509AttributeArchiveKey.InitializeEncode
: 
 - IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
: 
 - IX509AttributeArchiveKeyHash.InitializeDecode
: 
 - IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob
: 
 - IX509AttributeClientId.get_ClientId
: 
 - IX509AttributeClientId.get_MachineDnsName
: 
 - IX509AttributeClientId.get_ProcessName
: 
 - IX509AttributeClientId.get_UserSamName
: 
 - IX509AttributeClientId.InitializeDecode
: 
 - IX509AttributeClientId.InitializeEncode
: 
 - IX509AttributeCspProvider.get_KeySpec
: 
 - IX509AttributeCspProvider.get_ProviderName
: 
 - IX509AttributeCspProvider.get_Signature
: 
 - IX509AttributeCspProvider.InitializeDecode
: 
 - IX509AttributeCspProvider.InitializeEncode
: 
 - IX509AttributeExtensions.get_X509Extensions
: 
 - IX509AttributeExtensions.InitializeDecode
: 
 - IX509AttributeExtensions.InitializeEncode
: 
 - IX509AttributeOSVersion.get_OSVersion
: 
 - IX509AttributeOSVersion.InitializeDecode
: 
 - IX509AttributeOSVersion.InitializeEncode
: 
 - IX509AttributeRenewalCertificate.get_RenewalCertificate
: 
 - IX509AttributeRenewalCertificate.InitializeDecode
: 
 - IX509AttributeRenewalCertificate.InitializeEncode
: 
 - IX509Attributes.Add
: 
 - IX509Attributes.Clear
: 
 - IX509Attributes.get_Count
: 
 - IX509Attributes.get_ItemByIndex
: 
 - IX509Attributes.get__NewEnum
: 
 - IX509Attributes.Remove
: 
 - IX509CertificateRequest.Encode
: 
 - IX509CertificateRequest.GetInnerRequest
: 
 - IX509CertificateRequest.get_AlternateSignatureAlgorithm
: 
 - IX509CertificateRequest.get_ClientId
: 
 - IX509CertificateRequest.get_CspInformations
: 
 - IX509CertificateRequest.get_EnrollmentContext
: 
 - IX509CertificateRequest.get_HashAlgorithm
: 
 - IX509CertificateRequest.get_ParentWindow
: 
 - IX509CertificateRequest.get_RawData
: 
 - IX509CertificateRequest.get_RenewalCertificate
: 
 - IX509CertificateRequest.get_Silent
: 
 - IX509CertificateRequest.get_SuppressDefaults
: 
 - IX509CertificateRequest.get_Type
: 
 - IX509CertificateRequest.get_UIContextMessage
: 
 - IX509CertificateRequest.Initialize
: 
 - IX509CertificateRequest.put_AlternateSignatureAlgorithm
: 
 - IX509CertificateRequest.put_ClientId
: 
 - IX509CertificateRequest.put_CspInformations
: 
 - IX509CertificateRequest.put_HashAlgorithm
: 
 - IX509CertificateRequest.put_ParentWindow
: 
 - IX509CertificateRequest.put_RenewalCertificate
: 
 - IX509CertificateRequest.put_Silent
: 
 - IX509CertificateRequest.put_SuppressDefaults
: 
 - IX509CertificateRequest.put_UIContextMessage
: 
 - IX509CertificateRequest.ResetForEncode
: 
 - IX509CertificateRequestCertificate.CheckPublicKeySignature
: 
 - IX509CertificateRequestCertificate.get_Issuer
: 
 - IX509CertificateRequestCertificate.get_NotAfter
: 
 - IX509CertificateRequestCertificate.get_NotBefore
: 
 - IX509CertificateRequestCertificate.get_SerialNumber
: 
 - IX509CertificateRequestCertificate.get_SignerCertificate
: 
 - IX509CertificateRequestCertificate.put_Issuer
: 
 - IX509CertificateRequestCertificate.put_NotAfter
: 
 - IX509CertificateRequestCertificate.put_NotBefore
: 
 - IX509CertificateRequestCertificate.put_SerialNumber
: 
 - IX509CertificateRequestCertificate.put_SignerCertificate
: 
 - IX509CertificateRequestCertificate2.get_PolicyServer
: 
 - IX509CertificateRequestCertificate2.get_Template
: 
 - IX509CertificateRequestCertificate2.InitializeFromPrivateKeyTemplate
: 
 - IX509CertificateRequestCertificate2.InitializeFromTemplate
: 
 - IX509CertificateRequestCmc.get_ArchivePrivateKey
: 
 - IX509CertificateRequestCmc.get_CriticalExtensions
: 
 - IX509CertificateRequestCmc.get_CryptAttributes
: 
 - IX509CertificateRequestCmc.get_EncryptedKeyHash
: 
 - IX509CertificateRequestCmc.get_EncryptionAlgorithm
: 
 - IX509CertificateRequestCmc.get_EncryptionStrength
: 
 - IX509CertificateRequestCmc.get_KeyArchivalCertificate
: 
 - IX509CertificateRequestCmc.get_NameValuePairs
: 
 - IX509CertificateRequestCmc.get_NullSigned
: 
 - IX509CertificateRequestCmc.get_SenderNonce
: 
 - IX509CertificateRequestCmc.get_SignatureInformation
: 
 - IX509CertificateRequestCmc.get_SignerCertificates
: 
 - IX509CertificateRequestCmc.get_SuppressOids
: 
 - IX509CertificateRequestCmc.get_TemplateObjectId
: 
 - IX509CertificateRequestCmc.get_TransactionId
: 
 - IX509CertificateRequestCmc.get_X509Extensions
: 
 - IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName
: 
 - IX509CertificateRequestCmc.put_ArchivePrivateKey
: 
 - IX509CertificateRequestCmc.put_EncryptionAlgorithm
: 
 - IX509CertificateRequestCmc.put_EncryptionStrength
: 
 - IX509CertificateRequestCmc.put_KeyArchivalCertificate
: 
 - IX509CertificateRequestCmc.put_SenderNonce
: 
 - IX509CertificateRequestCmc.put_TransactionId
: 
 - IX509CertificateRequestCmc2.CheckCertificateSignature
: 
 - IX509CertificateRequestCmc2.CheckSignature
: 
 - IX509CertificateRequestCmc2.get_PolicyServer
: 
 - IX509CertificateRequestCmc2.get_Template
: 
 - IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate
: 
 - IX509CertificateRequestCmc2.InitializeFromTemplate
: 
 - IX509CertificateRequestPkcs10.CheckSignature
: 
 - IX509CertificateRequestPkcs10.GetCspStatuses
: 
 - IX509CertificateRequestPkcs10.get_CriticalExtensions
: 
 - IX509CertificateRequestPkcs10.get_CryptAttributes
: 
 - IX509CertificateRequestPkcs10.get_CspStatuses
: 
 - IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix
: 
 - IX509CertificateRequestPkcs10.get_NullSigned
: 
 - IX509CertificateRequestPkcs10.get_OldCertificate
: 
 - IX509CertificateRequestPkcs10.get_PrivateKey
: 
 - IX509CertificateRequestPkcs10.get_PublicKey
: 
 - IX509CertificateRequestPkcs10.get_RawDataToBeSigned
: 
 - IX509CertificateRequestPkcs10.get_ReuseKey
: 
 - IX509CertificateRequestPkcs10.get_Signature
: 
 - IX509CertificateRequestPkcs10.get_SignatureInformation
: 
 - IX509CertificateRequestPkcs10.get_SmimeCapabilities
: 
 - IX509CertificateRequestPkcs10.get_Subject
: 
 - IX509CertificateRequestPkcs10.get_SuppressOids
: 
 - IX509CertificateRequestPkcs10.get_TemplateObjectId
: 
 - IX509CertificateRequestPkcs10.get_X509Extensions
: 
 - IX509CertificateRequestPkcs10.InitializeDecode
: 
 - IX509CertificateRequestPkcs10.InitializeFromCertificate
: 
 - IX509CertificateRequestPkcs10.InitializeFromPrivateKey
: 
 - IX509CertificateRequestPkcs10.InitializeFromPublicKey
: 
 - IX509CertificateRequestPkcs10.InitializeFromTemplateName
: 
 - IX509CertificateRequestPkcs10.IsSmartCard
: 
 - IX509CertificateRequestPkcs10.put_KeyContainerNamePrefix
: 
 - IX509CertificateRequestPkcs10.put_SmimeCapabilities
: 
 - IX509CertificateRequestPkcs10.put_Subject
: 
 - IX509CertificateRequestPkcs10V2.get_PolicyServer
: 
 - IX509CertificateRequestPkcs10V2.get_Template
: 
 - IX509CertificateRequestPkcs10V2.InitializeFromPrivateKeyTemplate
: 
 - IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate
: 
 - IX509CertificateRequestPkcs10V2.InitializeFromTemplate
: 
 - IX509CertificateRequestPkcs10V3.get_AttestationEncryptionCertificate
: 
 - IX509CertificateRequestPkcs10V3.get_AttestPrivateKey
: 
 - IX509CertificateRequestPkcs10V3.get_ChallengePassword
: 
 - IX509CertificateRequestPkcs10V3.get_EncryptionAlgorithm
: 
 - IX509CertificateRequestPkcs10V3.get_EncryptionStrength
: 
 - IX509CertificateRequestPkcs10V3.get_NameValuePairs
: 
 - IX509CertificateRequestPkcs10V3.put_AttestationEncryptionCertificate
: 
 - IX509CertificateRequestPkcs10V3.put_AttestPrivateKey
: 
 - IX509CertificateRequestPkcs10V3.put_ChallengePassword
: 
 - IX509CertificateRequestPkcs10V3.put_EncryptionAlgorithm
: 
 - IX509CertificateRequestPkcs10V3.put_EncryptionStrength
: 
 - IX509CertificateRequestPkcs7.get_RequesterName
: 
 - IX509CertificateRequestPkcs7.get_SignerCertificate
: 
 - IX509CertificateRequestPkcs7.InitializeDecode
: 
 - IX509CertificateRequestPkcs7.InitializeFromCertificate
: 
 - IX509CertificateRequestPkcs7.InitializeFromInnerRequest
: 
 - IX509CertificateRequestPkcs7.InitializeFromTemplateName
: 
 - IX509CertificateRequestPkcs7.put_RequesterName
: 
 - IX509CertificateRequestPkcs7.put_SignerCertificate
: 
 - IX509CertificateRequestPkcs7V2.CheckCertificateSignature
: 
 - IX509CertificateRequestPkcs7V2.get_PolicyServer
: 
 - IX509CertificateRequestPkcs7V2.get_Template
: 
 - IX509CertificateRequestPkcs7V2.InitializeFromTemplate
: 
 - IX509CertificateTemplate.get_Property
: 
 - IX509CertificateTemplates.Add
: 
 - IX509CertificateTemplates.Clear
: 
 - IX509CertificateTemplates.get_Count
: 
 - IX509CertificateTemplates.get_ItemByIndex
: 
 - IX509CertificateTemplates.get_ItemByName
: 
 - IX509CertificateTemplates.get_ItemByOid
: 
 - IX509CertificateTemplates.get__NewEnum
: 
 - IX509CertificateTemplates.Remove
: 
 - IX509CertificateTemplateWritable.Commit
: 
 - IX509CertificateTemplateWritable.get_Property
: 
 - IX509CertificateTemplateWritable.get_Template
: 
 - IX509CertificateTemplateWritable.Initialize
: 
 - IX509CertificateTemplateWritable.put_Property
: 
 - IX509EndorsementKey.AddCertificate
: 
 - IX509EndorsementKey.Close
: 
 - IX509EndorsementKey.ExportPublicKey
: 
 - IX509EndorsementKey.GetCertificateByIndex
: 
 - IX509EndorsementKey.GetCertificateCount
: 
 - IX509EndorsementKey.get_Length
: 
 - IX509EndorsementKey.get_Opened
: 
 - IX509EndorsementKey.get_ProviderName
: 
 - IX509EndorsementKey.Open
: 
 - IX509EndorsementKey.put_ProviderName
: 
 - IX509EndorsementKey.RemoveCertificate
: 
 - IX509Enrollment.CreatePFX
: 
 - IX509Enrollment.CreateRequest
: 
 - IX509Enrollment.Enroll
: 
 - IX509Enrollment.get_CAConfigString
: 
 - IX509Enrollment.get_Certificate
: 
 - IX509Enrollment.get_CertificateDescription
: 
 - IX509Enrollment.get_CertificateFriendlyName
: 
 - IX509Enrollment.get_EnrollmentContext
: 
 - IX509Enrollment.get_NameValuePairs
: 
 - IX509Enrollment.get_ParentWindow
: 
 - IX509Enrollment.get_Request
: 
 - IX509Enrollment.get_RequestId
: 
 - IX509Enrollment.get_Response
: 
 - IX509Enrollment.get_Silent
: 
 - IX509Enrollment.get_Status
: 
 - IX509Enrollment.Initialize
: 
 - IX509Enrollment.InitializeFromRequest
: 
 - IX509Enrollment.InitializeFromTemplateName
: 
 - IX509Enrollment.InstallResponse
: 
 - IX509Enrollment.put_CertificateDescription
: 
 - IX509Enrollment.put_CertificateFriendlyName
: 
 - IX509Enrollment.put_ParentWindow
: 
 - IX509Enrollment.put_Silent
: 
 - IX509Enrollment2.get_PolicyServer
: 
 - IX509Enrollment2.get_RequestIdString
: 
 - IX509Enrollment2.get_Template
: 
 - IX509Enrollment2.InitializeFromTemplate
: 
 - IX509Enrollment2.InstallResponse2
: 
 - IX509EnrollmentHelper.AddEnrollmentServer
: 
 - IX509EnrollmentHelper.AddPolicyServer
: 
 - IX509EnrollmentHelper.Enroll
: 
 - IX509EnrollmentHelper.Initialize
: 
 - IX509EnrollmentPolicyServer.Export
: 
 - IX509EnrollmentPolicyServer.GetAllowUnTrustedCA
: 
 - IX509EnrollmentPolicyServer.GetAuthFlags
: 
 - IX509EnrollmentPolicyServer.GetCacheDir
: 
 - IX509EnrollmentPolicyServer.GetCachePath
: 
 - IX509EnrollmentPolicyServer.GetCAs
: 
 - IX509EnrollmentPolicyServer.GetCAsForTemplate
: 
 - IX509EnrollmentPolicyServer.GetCustomOids
: 
 - IX509EnrollmentPolicyServer.GetFriendlyName
: 
 - IX509EnrollmentPolicyServer.GetIsDefaultCEP
: 
 - IX509EnrollmentPolicyServer.GetLastUpdateTime
: 
 - IX509EnrollmentPolicyServer.GetNextUpdateTime
: 
 - IX509EnrollmentPolicyServer.GetPolicyServerId
: 
 - IX509EnrollmentPolicyServer.GetPolicyServerUrl
: 
 - IX509EnrollmentPolicyServer.GetTemplates
: 
 - IX509EnrollmentPolicyServer.GetUseClientId
: 
 - IX509EnrollmentPolicyServer.get_Cost
: 
 - IX509EnrollmentPolicyServer.Initialize
: 
 - IX509EnrollmentPolicyServer.InitializeImport
: 
 - IX509EnrollmentPolicyServer.LoadPolicy
: 
 - IX509EnrollmentPolicyServer.put_Cost
: 
 - IX509EnrollmentPolicyServer.QueryChanges
: 
 - IX509EnrollmentPolicyServer.SetCredential
: 
 - IX509EnrollmentPolicyServer.Validate
: 
 - IX509EnrollmentStatus.AppendText
: 
 - IX509EnrollmentStatus.get_Display
: 
 - IX509EnrollmentStatus.get_Error
: 
 - IX509EnrollmentStatus.get_ErrorText
: 
 - IX509EnrollmentStatus.get_Selected
: 
 - IX509EnrollmentStatus.get_Status
: 
 - IX509EnrollmentStatus.get_Text
: 
 - IX509EnrollmentStatus.put_Display
: 
 - IX509EnrollmentStatus.put_Error
: 
 - IX509EnrollmentStatus.put_Selected
: 
 - IX509EnrollmentStatus.put_Status
: 
 - IX509EnrollmentStatus.put_Text
: 
 - IX509EnrollmentWebClassFactory.CreateObject
: 
 - IX509Extension.get_Critical
: 
 - IX509Extension.get_ObjectId
: 
 - IX509Extension.get_RawData
: 
 - IX509Extension.Initialize
: 
 - IX509Extension.put_Critical
: 
 - IX509ExtensionAlternativeNames.get_AlternativeNames
: 
 - IX509ExtensionAlternativeNames.InitializeDecode
: 
 - IX509ExtensionAlternativeNames.InitializeEncode
: 
 - IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier
: 
 - IX509ExtensionAuthorityKeyIdentifier.InitializeDecode
: 
 - IX509ExtensionAuthorityKeyIdentifier.InitializeEncode
: 
 - IX509ExtensionBasicConstraints.get_IsCA
: 
 - IX509ExtensionBasicConstraints.get_PathLenConstraint
: 
 - IX509ExtensionBasicConstraints.InitializeDecode
: 
 - IX509ExtensionBasicConstraints.InitializeEncode
: 
 - IX509ExtensionCertificatePolicies.get_Policies
: 
 - IX509ExtensionCertificatePolicies.InitializeDecode
: 
 - IX509ExtensionCertificatePolicies.InitializeEncode
: 
 - IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage
: 
 - IX509ExtensionEnhancedKeyUsage.InitializeDecode
: 
 - IX509ExtensionEnhancedKeyUsage.InitializeEncode
: 
 - IX509ExtensionKeyUsage.get_KeyUsage
: 
 - IX509ExtensionKeyUsage.InitializeDecode
: 
 - IX509ExtensionKeyUsage.InitializeEncode
: 
 - IX509ExtensionMSApplicationPolicies.get_Policies
: 
 - IX509ExtensionMSApplicationPolicies.InitializeDecode
: 
 - IX509ExtensionMSApplicationPolicies.InitializeEncode
: 
 - IX509Extensions.Add
: 
 - IX509Extensions.AddRange
: 
 - IX509Extensions.Clear
: 
 - IX509Extensions.get_Count
: 
 - IX509Extensions.get_IndexByObjectId
: 
 - IX509Extensions.get_ItemByIndex
: 
 - IX509Extensions.get__NewEnum
: 
 - IX509Extensions.Remove
: 
 - IX509ExtensionSmimeCapabilities.get_SmimeCapabilities
: 
 - IX509ExtensionSmimeCapabilities.InitializeDecode
: 
 - IX509ExtensionSmimeCapabilities.InitializeEncode
: 
 - IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier
: 
 - IX509ExtensionSubjectKeyIdentifier.InitializeDecode
: 
 - IX509ExtensionSubjectKeyIdentifier.InitializeEncode
: 
 - IX509ExtensionTemplate.get_MajorVersion
: 
 - IX509ExtensionTemplate.get_MinorVersion
: 
 - IX509ExtensionTemplate.get_TemplateOid
: 
 - IX509ExtensionTemplate.InitializeDecode
: 
 - IX509ExtensionTemplate.InitializeEncode
: 
 - IX509ExtensionTemplateName.get_TemplateName
: 
 - IX509ExtensionTemplateName.InitializeDecode
: 
 - IX509ExtensionTemplateName.InitializeEncode
: 
 - IX509MachineEnrollmentFactory.CreateObject
: 
 - IX509NameValuePair.get_Name
: 
 - IX509NameValuePair.get_Value
: 
 - IX509NameValuePair.Initialize
: 
 - IX509NameValuePairs.Add
: 
 - IX509NameValuePairs.Clear
: 
 - IX509NameValuePairs.get_Count
: 
 - IX509NameValuePairs.get_ItemByIndex
: 
 - IX509NameValuePairs.get__NewEnum
: 
 - IX509NameValuePairs.Remove
: 
 - IX509PolicyServerListManager.Add
: 
 - IX509PolicyServerListManager.Clear
: 
 - IX509PolicyServerListManager.get_Count
: 
 - IX509PolicyServerListManager.get_ItemByIndex
: 
 - IX509PolicyServerListManager.get__NewEnum
: 
 - IX509PolicyServerListManager.Initialize
: 
 - IX509PolicyServerListManager.Remove
: 
 - IX509PolicyServerUrl.GetStringProperty
: 
 - IX509PolicyServerUrl.get_AuthFlags
: 
 - IX509PolicyServerUrl.get_Cost
: 
 - IX509PolicyServerUrl.get_Default
: 
 - IX509PolicyServerUrl.get_Flags
: 
 - IX509PolicyServerUrl.get_Url
: 
 - IX509PolicyServerUrl.Initialize
: 
 - IX509PolicyServerUrl.put_AuthFlags
: 
 - IX509PolicyServerUrl.put_Cost
: 
 - IX509PolicyServerUrl.put_Default
: 
 - IX509PolicyServerUrl.put_Flags
: 
 - IX509PolicyServerUrl.put_Url
: 
 - IX509PolicyServerUrl.RemoveFromRegistry
: 
 - IX509PolicyServerUrl.SetStringProperty
: 
 - IX509PolicyServerUrl.UpdateRegistry
: 
 - IX509PrivateKey.Close
: 
 - IX509PrivateKey.Create
: 
 - IX509PrivateKey.Delete
: 
 - IX509PrivateKey.Export
: 
 - IX509PrivateKey.ExportPublicKey
: 
 - IX509PrivateKey.get_Algorithm
: 
 - IX509PrivateKey.get_Certificate
: 
 - IX509PrivateKey.get_ContainerName
: 
 - IX509PrivateKey.get_ContainerNamePrefix
: 
 - IX509PrivateKey.get_CspInformations
: 
 - IX509PrivateKey.get_CspStatus
: 
 - IX509PrivateKey.get_DefaultContainer
: 
 - IX509PrivateKey.get_Description
: 
 - IX509PrivateKey.get_Existing
: 
 - IX509PrivateKey.get_ExportPolicy
: 
 - IX509PrivateKey.get_FriendlyName
: 
 - IX509PrivateKey.get_KeyProtection
: 
 - IX509PrivateKey.get_KeySpec
: 
 - IX509PrivateKey.get_KeyUsage
: 
 - IX509PrivateKey.get_LegacyCsp
: 
 - IX509PrivateKey.get_Length
: 
 - IX509PrivateKey.get_MachineContext
: 
 - IX509PrivateKey.get_Opened
: 
 - IX509PrivateKey.get_ParentWindow
: 
 - IX509PrivateKey.get_ProviderName
: 
 - IX509PrivateKey.get_ProviderType
: 
 - IX509PrivateKey.get_ReaderName
: 
 - IX509PrivateKey.get_SecurityDescriptor
: 
 - IX509PrivateKey.get_Silent
: 
 - IX509PrivateKey.get_UIContextMessage
: 
 - IX509PrivateKey.get_UniqueContainerName
: 
 - IX509PrivateKey.Import
: 
 - IX509PrivateKey.Open
: 
 - IX509PrivateKey.put_Algorithm
: 
 - IX509PrivateKey.put_Certificate
: 
 - IX509PrivateKey.put_ContainerName
: 
 - IX509PrivateKey.put_ContainerNamePrefix
: 
 - IX509PrivateKey.put_CspInformations
: 
 - IX509PrivateKey.put_CspStatus
: 
 - IX509PrivateKey.put_Description
: 
 - IX509PrivateKey.put_Existing
: 
 - IX509PrivateKey.put_ExportPolicy
: 
 - IX509PrivateKey.put_FriendlyName
: 
 - IX509PrivateKey.put_KeyProtection
: 
 - IX509PrivateKey.put_KeySpec
: 
 - IX509PrivateKey.put_KeyUsage
: 
 - IX509PrivateKey.put_LegacyCsp
: 
 - IX509PrivateKey.put_Length
: 
 - IX509PrivateKey.put_MachineContext
: 
 - IX509PrivateKey.put_ParentWindow
: 
 - IX509PrivateKey.put_Pin
: 
 - IX509PrivateKey.put_ProviderName
: 
 - IX509PrivateKey.put_ProviderType
: 
 - IX509PrivateKey.put_ReaderName
: 
 - IX509PrivateKey.put_SecurityDescriptor
: 
 - IX509PrivateKey.put_Silent
: 
 - IX509PrivateKey.put_UIContextMessage
: 
 - IX509PrivateKey.Verify
: 
 - IX509PublicKey.ComputeKeyIdentifier
: 
 - IX509PublicKey.get_Algorithm
: 
 - IX509PublicKey.get_EncodedKey
: 
 - IX509PublicKey.get_EncodedParameters
: 
 - IX509PublicKey.get_Length
: 
 - IX509PublicKey.Initialize
: 
 - IX509PublicKey.InitializeFromEncodedPublicKeyInfo
: 
 - IX509SCEPEnrollment.CreateRequestMessage
: 
 - IX509SCEPEnrollment.CreateRetrieveCertificateMessage
: 
 - IX509SCEPEnrollment.CreateRetrievePendingMessage
: 
 - IX509SCEPEnrollment.DeleteRequest
: 
 - IX509SCEPEnrollment.get_Certificate
: 
 - IX509SCEPEnrollment.get_CertificateFriendlyName
: 
 - IX509SCEPEnrollment.get_FailInfo
: 
 - IX509SCEPEnrollment.get_OldCertificate
: 
 - IX509SCEPEnrollment.get_Request
: 
 - IX509SCEPEnrollment.get_SignerCertificate
: 
 - IX509SCEPEnrollment.get_Status
: 
 - IX509SCEPEnrollment.get_TransactionId
: 
 - IX509SCEPEnrollment.Initialize
: 
 - IX509SCEPEnrollment.InitializeForPending
: 
 - IX509SCEPEnrollment.ProcessResponseMessage
: 
 - IX509SCEPEnrollment.put_CertificateFriendlyName
: 
 - IX509SCEPEnrollment.put_OldCertificate
: 
 - IX509SCEPEnrollment.put_ServerCapabilities
: 
 - IX509SCEPEnrollment.put_SignerCertificate
: 
 - IX509SCEPEnrollment.put_Silent
: 
 - IX509SCEPEnrollment.put_TransactionId
: 
 - IX509SignatureInformation.GetSignatureAlgorithm
: 
 - IX509SignatureInformation.get_AlternateSignatureAlgorithm
: 
 - IX509SignatureInformation.get_AlternateSignatureAlgorithmSet
: 
 - IX509SignatureInformation.get_HashAlgorithm
: 
 - IX509SignatureInformation.get_NullSigned
: 
 - IX509SignatureInformation.get_Parameters
: 
 - IX509SignatureInformation.get_PublicKeyAlgorithm
: 
 - IX509SignatureInformation.put_AlternateSignatureAlgorithm
: 
 - IX509SignatureInformation.put_HashAlgorithm
: 
 - IX509SignatureInformation.put_NullSigned
: 
 - IX509SignatureInformation.put_Parameters
: 
 - IX509SignatureInformation.put_PublicKeyAlgorithm
: 
 - IX509SignatureInformation.SetDefaultValues
: 
 - IAlternativeName
: 
 - IAlternativeNames
: 
 - IBinaryConverter
: 
 - ICertificateAttestationChallenge
: 
 - ICertificatePolicies
: 
 - ICertificatePolicy
: 
 - ICertificationAuthorities
: 
 - ICertificationAuthority
: 
 - ICertProperties
: 
 - ICertProperty
: 
 - ICertPropertyArchived
: 
 - ICertPropertyArchivedKeyHash
: 
 - ICertPropertyAutoEnroll
: 
 - ICertPropertyBackedUp
: 
 - ICertPropertyDescription
: 
 - ICertPropertyEnrollment
: 
 - ICertPropertyEnrollmentPolicyServer
: 
 - ICertPropertyFriendlyName
: 
 - ICertPropertyKeyProvInfo
: 
 - ICertPropertyRenewal
: 
 - ICertPropertyRequestOriginator
: 
 - ICertPropertySHA1Hash
: 
 - ICryptAttribute
: 
 - ICryptAttributes
: 
 - ICspAlgorithm
: 
 - ICspAlgorithms
: 
 - ICspInformation
: 
 - ICspInformations
: 
 - ICspStatus
: 
 - ICspStatuses
: 
 - IObjectId
: 
 - IObjectIds
: 
 - IPolicyQualifier
: 
 - IPolicyQualifiers
: 
 - ISignerCertificate
: 
 - ISignerCertificates
: 
 - ISmimeCapabilities
: 
 - ISmimeCapability
: 
 - IX500DistinguishedName
: 
 - IX509Attribute
: 
 - IX509AttributeArchiveKey
: 
 - IX509AttributeArchiveKeyHash
: 
 - IX509AttributeClientId
: 
 - IX509AttributeCspProvider
: 
 - IX509AttributeExtensions
: 
 - IX509AttributeOSVersion
: 
 - IX509AttributeRenewalCertificate
: 
 - IX509Attributes
: 
 - IX509CertificateRequest
: 
 - IX509CertificateRequestCertificate
: 
 - IX509CertificateRequestCertificate2
: 
 - IX509CertificateRequestCmc
: 
 - IX509CertificateRequestCmc2
: 
 - IX509CertificateRequestPkcs10
: 
 - IX509CertificateRequestPkcs10V2
: 
 - IX509CertificateRequestPkcs10V3
: 
 - IX509CertificateRequestPkcs7
: 
 - IX509CertificateRequestPkcs7V2
: 
 - IX509CertificateTemplate
: 
 - IX509CertificateTemplates
: 
 - IX509CertificateTemplateWritable
: 
 - IX509EndorsementKey
: 
 - IX509Enrollment
: 
 - IX509Enrollment2
: 
 - IX509EnrollmentHelper
: 
 - IX509EnrollmentPolicyServer
: 
 - IX509EnrollmentStatus
: 
 - IX509EnrollmentWebClassFactory
: 
 - IX509Extension
: 
 - IX509ExtensionAlternativeNames
: 
 - IX509ExtensionAuthorityKeyIdentifier
: 
 - IX509ExtensionBasicConstraints
: 
 - IX509ExtensionCertificatePolicies
: 
 - IX509ExtensionEnhancedKeyUsage
: 
 - IX509ExtensionKeyUsage
: 
 - IX509ExtensionMSApplicationPolicies
: 
 - IX509Extensions
: 
 - IX509ExtensionSmimeCapabilities
: 
 - IX509ExtensionSubjectKeyIdentifier
: 
 - IX509ExtensionTemplate
: 
 - IX509ExtensionTemplateName
: 
 - IX509MachineEnrollmentFactory
: 
 - IX509NameValuePair
: 
 - IX509NameValuePairs
: 
 - IX509PolicyServerListManager
: 
 - IX509PolicyServerUrl
: 
 - IX509PrivateKey
: 
 - IX509PublicKey
: 
 - IX509SCEPEnrollment
: 
 - IX509SignatureInformation
: 
 - certexit.h
: 
 - ICertExit.GetDescription
: 
 - ICertExit.Initialize
: 
 - ICertExit.Notify
: 
 - ICertExit2.GetManageModule
: 
 - ICertExit
: 
 - ICertExit2
: 
 - certif.h
: 
 - ICertServerExit.EnumerateAttributes
: 
 - ICertServerExit.EnumerateAttributesClose
: 
 - ICertServerExit.EnumerateAttributesSetup
: 
 - ICertServerExit.EnumerateExtensions
: 
 - ICertServerExit.EnumerateExtensionsClose
: 
 - ICertServerExit.EnumerateExtensionsSetup
: 
 - ICertServerExit.GetCertificateExtension
: 
 - ICertServerExit.GetCertificateExtensionFlags
: 
 - ICertServerExit.GetCertificateProperty
: 
 - ICertServerExit.GetRequestAttribute
: 
 - ICertServerExit.GetRequestProperty
: 
 - ICertServerExit.SetContext
: 
 - ICertServerPolicy.EnumerateAttributes
: 
 - ICertServerPolicy.EnumerateAttributesClose
: 
 - ICertServerPolicy.EnumerateAttributesSetup
: 
 - ICertServerPolicy.EnumerateExtensions
: 
 - ICertServerPolicy.EnumerateExtensionsClose
: 
 - ICertServerPolicy.EnumerateExtensionsSetup
: 
 - ICertServerPolicy.GetCertificateExtension
: 
 - ICertServerPolicy.GetCertificateExtensionFlags
: 
 - ICertServerPolicy.GetCertificateProperty
: 
 - ICertServerPolicy.GetRequestAttribute
: 
 - ICertServerPolicy.GetRequestProperty
: 
 - ICertServerPolicy.SetCertificateExtension
: 
 - ICertServerPolicy.SetCertificateProperty
: 
 - ICertServerPolicy.SetContext
: 
 - ICertServerExit
: 
 - ICertServerPolicy
: 
 - certmod.h
: 
 - ICertManageModule.Configure
: 
 - ICertManageModule.GetProperty
: 
 - ICertManageModule.SetProperty
: 
 - ICertManageModule
: 
 - certpol.h
: 
 - X509SCEPDisposition
: 
 - X509SCEPFailInfo
: 
 - ICertPolicy.GetDescription
: 
 - ICertPolicy.Initialize
: 
 - ICertPolicy.ShutDown
: 
 - ICertPolicy.VerifyRequest
: 
 - ICertPolicy2.GetManageModule
: 
 - INDESPolicy.GenerateChallenge
: 
 - INDESPolicy.Initialize
: 
 - INDESPolicy.Notify
: 
 - INDESPolicy.Uninitialize
: 
 - INDESPolicy.VerifyRequest
: 
 - ICertPolicy
: 
 - ICertPolicy2
: 
 - INDESPolicy
: 
 - PstAcquirePrivateKey
: 
 - PstGetCertificates
: 
 - PstGetTrustAnchors
: 
 - PstGetUserNameForCertificate
: 
 - PstMapCertificate
: 
 - PstValidate
: 
 - certsrv.h
: 
 - ENUM_CATYPES
: 
 - certview.h
: 
 - ICertView.EnumCertViewColumn
: 
 - ICertView.GetColumnCount
: 
 - ICertView.GetColumnIndex
: 
 - ICertView.OpenConnection
: 
 - ICertView.OpenView
: 
 - ICertView.SetRestriction
: 
 - ICertView.SetResultColumn
: 
 - ICertView.SetResultColumnCount
: 
 - ICertView2.SetTable
: 
 - IEnumCERTVIEWATTRIBUTE.Clone
: 
 - IEnumCERTVIEWATTRIBUTE.GetName
: 
 - IEnumCERTVIEWATTRIBUTE.GetValue
: 
 - IEnumCERTVIEWATTRIBUTE.Next
: 
 - IEnumCERTVIEWATTRIBUTE.Reset
: 
 - IEnumCERTVIEWATTRIBUTE.Skip
: 
 - IEnumCERTVIEWCOLUMN.Clone
: 
 - IEnumCERTVIEWCOLUMN.GetDisplayName
: 
 - IEnumCERTVIEWCOLUMN.GetMaxLength
: 
 - IEnumCERTVIEWCOLUMN.GetName
: 
 - IEnumCERTVIEWCOLUMN.GetType
: 
 - IEnumCERTVIEWCOLUMN.GetValue
: 
 - IEnumCERTVIEWCOLUMN.IsIndexed
: 
 - IEnumCERTVIEWCOLUMN.Next
: 
 - IEnumCERTVIEWCOLUMN.Reset
: 
 - IEnumCERTVIEWCOLUMN.Skip
: 
 - IEnumCERTVIEWEXTENSION.Clone
: 
 - IEnumCERTVIEWEXTENSION.GetFlags
: 
 - IEnumCERTVIEWEXTENSION.GetName
: 
 - IEnumCERTVIEWEXTENSION.GetValue
: 
 - IEnumCERTVIEWEXTENSION.Next
: 
 - IEnumCERTVIEWEXTENSION.Reset
: 
 - IEnumCERTVIEWEXTENSION.Skip
: 
 - IEnumCERTVIEWROW.EnumCertViewAttribute
: 
 - IEnumCERTVIEWROW.EnumCertViewColumn
: 
 - IEnumCERTVIEWROW.EnumCertViewExtension
: 
 - IEnumCERTVIEWROW.GetMaxIndex
: 
 - IEnumCERTVIEWROW.Next
: 
 - IEnumCERTVIEWROW.Reset
: 
 - IEnumCERTVIEWROW.Skip
: 
 - ICertView
: 
 - ICertView2
: 
 - IEnumCERTVIEWATTRIBUTE
: 
 - IEnumCERTVIEWCOLUMN
: 
 - IEnumCERTVIEWEXTENSION
: 
 - IEnumCERTVIEWROW
: 
 - cfg.h
: 
 - _PNP_VETO_TYPE
: 
 - cfgmgr32.h
: 
 - _CM_NOTIFY_ACTION
: 
 - CM_Add_Empty_Log_Conf
: 
 - CM_Add_Empty_Log_Conf_Ex
: 
 - CM_Add_IDW
: 
 - CM_Add_ID_ExW
: 
 - CM_Add_Res_Des
: 
 - CM_Add_Res_Des_Ex
: 
 - CM_Connect_MachineW
: 
 - CM_Delete_Class_Key
: 
 - CM_Delete_Device_Interface_KeyW
: 
 - CM_Delete_Device_Interface_Key_ExA
: 
 - CM_Delete_Device_Interface_Key_ExW
: 
 - CM_Delete_DevNode_Key
: 
 - CM_Disable_DevNode
: 
 - CM_Disconnect_Machine
: 
 - CM_Enable_DevNode
: 
 - CM_Enumerate_Classes
: 
 - CM_Enumerate_Classes_Ex
: 
 - CM_Enumerate_EnumeratorsW
: 
 - CM_Enumerate_Enumerators_ExW
: 
 - CM_Free_Log_Conf
: 
 - CM_Free_Log_Conf_Ex
: 
 - CM_Free_Log_Conf_Handle
: 
 - CM_Free_Resource_Conflict_Handle
: 
 - CM_Free_Res_Des
: 
 - CM_Free_Res_Des_Ex
: 
 - CM_Free_Res_Des_Handle
: 
 - CM_Get_Child
: 
 - CM_Get_Child_Ex
: 
 - CM_Get_Class_PropertyW
: 
 - CM_Get_Class_Property_ExW
: 
 - CM_Get_Class_Property_Keys
: 
 - CM_Get_Class_Property_Keys_Ex
: 
 - CM_Get_Class_Registry_PropertyW
: 
 - CM_Get_Depth
: 
 - CM_Get_Depth_Ex
: 
 - CM_Get_Device_IDW
: 
 - CM_Get_Device_ID_ExW
: 
 - CM_Get_Device_ID_ListA
: 
 - CM_Get_Device_ID_ListW
: 
 - CM_Get_Device_ID_List_ExW
: 
 - CM_Get_Device_ID_List_SizeA
: 
 - CM_Get_Device_ID_List_SizeW
: 
 - CM_Get_Device_ID_List_Size_ExW
: 
 - CM_Get_Device_ID_Size
: 
 - CM_Get_Device_ID_Size_Ex
: 
 - CM_Get_Device_Interface_AliasW
: 
 - CM_Get_Device_Interface_ListA
: 
 - CM_Get_Device_Interface_ListW
: 
 - CM_Get_Device_Interface_List_SizeA
: 
 - CM_Get_Device_Interface_List_SizeW
: 
 - CM_Get_Device_Interface_PropertyW
: 
 - CM_Get_Device_Interface_Property_ExW
: 
 - CM_Get_Device_Interface_Property_KeysW
: 
 - CM_Get_Device_Interface_Property_Keys_ExW
: 
 - CM_Get_DevNode_PropertyW
: 
 - CM_Get_DevNode_Property_ExW
: 
 - CM_Get_DevNode_Property_Keys
: 
 - CM_Get_DevNode_Property_Keys_Ex
: 
 - CM_Get_DevNode_Registry_PropertyW
: 
 - CM_Get_DevNode_Status
: 
 - CM_Get_DevNode_Status_Ex
: 
 - CM_Get_First_Log_Conf
: 
 - CM_Get_First_Log_Conf_Ex
: 
 - CM_Get_HW_Prof_FlagsA
: 
 - CM_Get_HW_Prof_FlagsW
: 
 - CM_Get_HW_Prof_Flags_ExA
: 
 - CM_Get_HW_Prof_Flags_ExW
: 
 - CM_Get_Log_Conf_Priority
: 
 - CM_Get_Log_Conf_Priority_Ex
: 
 - CM_Get_Next_Log_Conf
: 
 - CM_Get_Next_Log_Conf_Ex
: 
 - CM_Get_Next_Res_Des
: 
 - CM_Get_Next_Res_Des_Ex
: 
 - CM_Get_Parent
: 
 - CM_Get_Parent_Ex
: 
 - CM_Get_Resource_Conflict_Count
: 
 - CM_Get_Resource_Conflict_DetailsW
: 
 - CM_Get_Res_Des_Data
: 
 - CM_Get_Res_Des_Data_Ex
: 
 - CM_Get_Res_Des_Data_Size
: 
 - CM_Get_Res_Des_Data_Size_Ex
: 
 - CM_Get_Sibling
: 
 - CM_Get_Sibling_Ex
: 
 - CM_Get_Version
: 
 - CM_Get_Version_Ex
: 
 - CM_Is_Dock_Station_Present
: 
 - CM_Is_Dock_Station_Present_Ex
: 
 - CM_Is_Version_Available
: 
 - CM_Is_Version_Available_Ex
: 
 - CM_Locate_DevNodeA
: 
 - CM_Locate_DevNodeW
: 
 - CM_Locate_DevNode_ExW
: 
 - CM_MapCrToWin32Err
: 
 - CM_Modify_Res_Des
: 
 - CM_Modify_Res_Des_Ex
: 
 - CM_Open_Class_KeyW
: 
 - CM_Open_Device_Interface_KeyA
: 
 - CM_Open_Device_Interface_KeyW
: 
 - CM_Open_Device_Interface_Key_ExA
: 
 - CM_Open_Device_Interface_Key_ExW
: 
 - CM_Open_DevNode_Key
: 
 - CM_Query_And_Remove_SubTreeW
: 
 - CM_Query_And_Remove_SubTree_ExW
: 
 - CM_Query_Resource_Conflict_List
: 
 - CM_Reenumerate_DevNode
: 
 - CM_Reenumerate_DevNode_Ex
: 
 - CM_Register_Notification
: 
 - CM_Request_Device_EjectW
: 
 - CM_Request_Device_Eject_ExW
: 
 - CM_Request_Eject_PC
: 
 - CM_Request_Eject_PC_Ex
: 
 - CM_Setup_DevNode
: 
 - CM_Set_Class_PropertyW
: 
 - CM_Set_Class_Property_ExW
: 
 - CM_Set_Class_Registry_PropertyW
: 
 - CM_Set_Device_Interface_PropertyW
: 
 - CM_Set_Device_Interface_Property_ExW
: 
 - CM_Set_DevNode_Problem
: 
 - CM_Set_DevNode_Problem_Ex
: 
 - CM_Set_DevNode_PropertyW
: 
 - CM_Set_DevNode_Property_ExW
: 
 - CM_Set_DevNode_Registry_PropertyW
: 
 - CM_Uninstall_DevNode
: 
 - CM_Unregister_Notification
: 
 - BusNumber_Des_s
: 
 - BusNumber_Range_s
: 
 - BusNumber_Resource_s
: 
 - CS_Des_s
: 
 - CS_Resource_s
: 
 - DMA_Des_s
: 
 - DMA_Range_s
: 
 - DMA_Resource_s
: 
 - IO_Des_s
: 
 - IO_Range_s
: 
 - IO_Resource_s
: 
 - IRQ_Des_32_s
: 
 - IRQ_Des_64_s
: 
 - IRQ_Range_s
: 
 - IRQ_Resource_32_s
: 
 - IRQ_Resource_64_s
: 
 - Mem_Des_s
: 
 - Mem_Range_s
: 
 - Mem_Resource_s
: 
 - MfCard_Des_s
: 
 - MfCard_Resource_s
: 
 - PcCard_Des_s
: 
 - PcCard_Resource_s
: 
 - _CM_NOTIFY_EVENT_DATA
: 
 - _CM_NOTIFY_FILTER
: 
 - _CONFLICT_DETAILS_A
: 
 - _CONFLICT_DETAILS_W
: 
 - chptrarr.h
: 
 - CHPtrArray.CHPtrArray
: 
 - CHPtrArray.GetAt
: 
 - CHPtrArray.GetSize
: 
 - CHPtrArray.RemoveAll
: 
 - CHPtrArray
: 
 - chstrarr.h
: 
 - CHStringArray.Add
: 
 - CHStringArray.Append
: 
 - CHStringArray.CHStringArray
: 
 - CHStringArray.Copy
: 
 - CHStringArray.ElementAt
: 
 - CHStringArray.FreeExtra
: 
 - CHStringArray.GetAt
: 
 - CHStringArray.GetData
: 
 - CHStringArray.GetSize
: 
 - CHStringArray.GetUpperBound
: 
 - CHStringArray.InsertAt
: 
 - CHStringArray.RemoveAll
: 
 - CHStringArray.RemoveAt
: 
 - CHStringArray.SetAt
: 
 - CHStringArray.SetAtGrow
: 
 - CHStringArray.SetSize
: 
 - CHStringArray
: 
 - chstring.h
: 
 - CHString.AllocSysString
: 
 - CHString.CHString
: 
 - CHString.Collate
: 
 - CHString.Compare
: 
 - CHString.CompareNoCase
: 
 - CHString.Empty
: 
 - CHString.Find
: 
 - CHString.FindOneOf
: 
 - CHString.Format
: 
 - CHString.FormatMessageW
: 
 - CHString.FormatV
: 
 - CHString.FreeExtra
: 
 - CHString.GetAllocLength
: 
 - CHString.GetAt
: 
 - CHString.GetBuffer
: 
 - CHString.GetBufferSetLength
: 
 - CHString.GetData
: 
 - CHString.GetLength
: 
 - CHString.IsEmpty
: 
 - CHString.Left
: 
 - CHString.LoadStringW
: 
 - CHString.LockBuffer
: 
 - CHString.MakeLower
: 
 - CHString.MakeReverse
: 
 - CHString.MakeUpper
: 
 - CHString.Mid
: 
 - CHString.operator LPCWSTR
: 
 - CHString.ReleaseBuffer
: 
 - CHString.ReverseFind
: 
 - CHString.Right
: 
 - CHString.SetAt
: 
 - CHString.SpanExcluding
: 
 - CHString.SpanIncluding
: 
 - CHString.TrimLeft
: 
 - CHString.TrimRight
: 
 - CHString.UnlockBuffer
: 
 - CHString
: 
 - clfs.h
: 
 - _CLFS_CONTEXT_MODE
: 
 - _CLFS_IOSTATS_CLASS
: 
 - _CLFS_LOG_ARCHIVE_MODE
: 
 - ClfsLsnEqual
: 
 - ClfsLsnGreater
: 
 - ClfsLsnLess
: 
 - ClfsLsnNull
: 
 - _CLFS_NODE_ID
: 
 - _CLS_ARCHIVE_DESCRIPTOR
: 
 - _CLS_CONTAINER_INFORMATION
: 
 - _CLS_INFORMATION
: 
 - _CLS_IO_STATISTICS
: 
 - _CLS_IO_STATISTICS_HEADER
: 
 - _CLS_LSN
: 
 - _CLS_SCAN_CONTEXT
: 
 - _CLS_WRITE_ENTRY
: 
 - clfsmgmt.h
: 
 - _CLFS_MGMT_POLICY_TYPE
: 
 - _CLFS_MGMT_NOTIFICATION
: 
 - _CLFS_MGMT_POLICY
: 
 - clfsmgmtw32.h
: 
 - PLOG_FULL_HANDLER_CALLBACK
: 
 - PLOG_TAIL_ADVANCE_CALLBACK
: 
 - PLOG_UNPINNED_CALLBACK
: 
 - DeregisterManageableLogClient
: 
 - HandleLogFull
: 
 - InstallLogPolicy
: 
 - LogTailAdvanceFailure
: 
 - QueryLogPolicy
: 
 - ReadLogNotification
: 
 - RegisterForLogWriteNotification
: 
 - RegisterManageableLogClient
: 
 - RemoveLogPolicy
: 
 - SetLogFileSizeWithPolicy
: 
 - _LOG_MANAGEMENT_CALLBACKS
: 
 - AddLogContainer
: 
 - AddLogContainerSet
: 
 - AdvanceLogBase
: 
 - AlignReservedLog
: 
 - AllocReservedLog
: 
 - CloseAndResetLogFile
: 
 - CreateLogContainerScanContext
: 
 - CreateLogFile
: 
 - CreateLogMarshallingArea
: 
 - DeleteLogByHandle
: 
 - DeleteLogFile
: 
 - DeleteLogMarshallingArea
: 
 - DumpLogRecords
: 
 - FlushLogBuffers
: 
 - FlushLogToLsn
: 
 - FreeReservedLog
: 
 - GetLogContainerName
: 
 - GetLogFileInformation
: 
 - GetLogIoStatistics
: 
 - GetNextLogArchiveExtent
: 
 - LsnBlockOffset
: 
 - LsnContainer
: 
 - LsnCreate
: 
 - LsnRecordSequence
: 
 - PrepareLogArchive
: 
 - ReadLogArchiveMetadata
: 
 - ReadLogRecord
: 
 - ReadLogRestartArea
: 
 - ReadNextLogRecord
: 
 - ReadPreviousLogRestartArea
: 
 - RemoveLogContainer
: 
 - RemoveLogContainerSet
: 
 - ReserveAndAppendLog
: 
 - ReserveAndAppendLogAligned
: 
 - ScanLogContainers
: 
 - SetEndOfLog
: 
 - SetLogArchiveMode
: 
 - SetLogArchiveTail
: 
 - TerminateLogArchive
: 
 - TerminateReadLog
: 
 - TruncateLog
: 
 - ValidateLog
: 
 - WriteLogRestartArea
: 
 - cloneviewhelper.h
: 
 - IViewHelper.Commit
: 
 - IViewHelper.GetActiveTopology
: 
 - IViewHelper.GetConnectedIDs
: 
 - IViewHelper.GetProceedOnNewConfiguration
: 
 - IViewHelper.SetActiveTopology
: 
 - IViewHelper.SetConfiguration
: 
 - tagAdapter
: 
 - tagAdapters
: 
 - tagDisplayMode
: 
 - tagDisplayModes
: 
 - tagSources
: 
 - cluadmex.h
: 
 - IGetClusterDataInfo.GetClusterHandle
: 
 - IGetClusterDataInfo.GetClusterName
: 
 - IGetClusterDataInfo.GetObjectCount
: 
 - IGetClusterGroupInfo.GetGroupHandle
: 
 - IGetClusterNetInterfaceInfo.GetNetInterfaceHandle
: 
 - IGetClusterNetworkInfo.GetNetworkHandle
: 
 - IGetClusterNodeInfo.GetNodeHandle
: 
 - IGetClusterObjectInfo.GetObjectName
: 
 - IGetClusterObjectInfo.GetObjectType
: 
 - IGetClusterResourceInfo.GetResourceHandle
: 
 - IGetClusterResourceInfo.GetResourceNetworkName
: 
 - IGetClusterResourceInfo.GetResourceTypeName
: 
 - IGetClusterUIInfo.GetClusterName
: 
 - IGetClusterUIInfo.GetFont
: 
 - IGetClusterUIInfo.GetIcon
: 
 - IGetClusterUIInfo.GetLocale
: 
 - IWCContextMenuCallback.AddExtensionMenuItem
: 
 - IWCPropertySheetCallback.AddPropertySheetPage
: 
 - IWCWizard97Callback.AddWizard97Page
: 
 - IWCWizard97Callback.EnableNext
: 
 - IWCWizardCallback.AddWizardPage
: 
 - IWCWizardCallback.EnableNext
: 
 - IWEExtendContextMenu.AddContextMenuItems
: 
 - IWEExtendPropertySheet.CreatePropertySheetPages
: 
 - IWEExtendWizard.CreateWizardPages
: 
 - IWEExtendWizard97.CreateWizard97Pages
: 
 - IWEInvokeCommand.InvokeCommand
: 
 - IGetClusterDataInfo
: 
 - IGetClusterGroupInfo
: 
 - IGetClusterNetInterfaceInfo
: 
 - IGetClusterNetworkInfo
: 
 - IGetClusterNodeInfo
: 
 - IGetClusterObjectInfo
: 
 - IGetClusterResourceInfo
: 
 - IGetClusterUIInfo
: 
 - IWCContextMenuCallback
: 
 - IWCPropertySheetCallback
: 
 - IWCWizard97Callback
: 
 - IWCWizardCallback
: 
 - IWEExtendContextMenu
: 
 - IWEExtendPropertySheet
: 
 - IWEExtendWizard
: 
 - IWEExtendWizard97
: 
 - IWEInvokeCommand
: 
 - clusapi.h
: 
 - PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY
: 
 - PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY
: 
 - PCLUSAPI_ADD_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY
: 
 - PCLUSAPI_ADD_CLUSTER_NODE
: 
---

# PCLUSAPI_ADD_CLUSTER_NODE callback function


## -description


Adds a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to an existing cluster. The <b>PCLUSAPI_ADD_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster, returned by the <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a> or 
       <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> function.


### -param lpszNodeName [in]

Name of the computer to add to the cluster.


### -param pfnProgressCallback [in, optional]

Optional address to a 
       <a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a> 
       callback function.


### -param pvCallbackArg [in, optional]

Argument for the callback function.


## -returns



Handle to the new node or <b>NULL</b> to indicate that the node was not successfully added 
       to the cluster. For more information about the error, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



After the <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> function successfully 
     completes, at least 30 seconds should be allowed before the 
     <i>AddClusterNode</i> function is called to add additional 
     nodes.




## -see-also




<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>



<a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
 

 

