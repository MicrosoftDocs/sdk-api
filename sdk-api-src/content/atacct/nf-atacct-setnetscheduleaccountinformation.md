---
UID: NF:atacct.SetNetScheduleAccountInformation
title: SetNetScheduleAccountInformation function
author: windows-sdk-content
description: The SetNetScheduleAccountInformation function sets the AT Service account name and password. The AT Service account name and password are used as the credentials for scheduled jobs created with NetScheduleJobAdd.
old-location: netmgmt\setnetscheduleaccountinformation.htm
old-project: NetMgmt
ms.assetid: e45cc3d6-f0dd-4c24-967e-4db08078d15e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: SetNetScheduleAccountInformation, SetNetScheduleAccountInformation function [Network Management], atacct/SetNetScheduleAccountInformation, netmgmt.setnetscheduleaccountinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: atacct.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	DllExport
 - HeaderDef
: 
api_location:
-	Mstask.dll
 - accctrl.h
: 
api_name:
-	SetNetScheduleAccountInformation
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
req.lib: Mstask.lib
req.dll: Mstask.dll
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
---

# SetNetScheduleAccountInformation function


## -description


<p class="CCE_Message">[<b>SetNetScheduleAccountInformation</b> is no longer available for use as of Windows 8. Instead, use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e"> Task Scheduler 2.0 Interfaces</a>.

]

The <b>SetNetScheduleAccountInformation</b> function sets the AT Service account name and password. The AT Service account name and password are used as the credentials for scheduled jobs created with <a href="https://msdn.microsoft.com/813d13ba-abe1-4b14-88c7-87ba88a42a3b">NetScheduleJobAdd</a>.


## -parameters




### -param pwszServerName [in]

A NULL-terminated wide character string for the name of the computer whose account information is being set.


### -param pwszAccount [in]

A pointer to a NULL-terminated wide character string for the account. To specify the local system account, set this parameter to <b>NULL</b>.


### -param pwszPassword [in]

A pointer to a NULL-terminated wide character string for the password. For information about securing password information, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


## -returns



The return value is an HRESULT. A value of S_OK indicates the account name and password were successfully set. Any other value indicates an error condition.

If the function fails, some of the possible return values are listed below. 

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x080070005</dt>
</dl>
</td>
<td width="60%">
Access was denied. This error is returned if the caller was not a member of the Administrators group. This error is also returned if the <i>pwszAccount</i> parameter  was  not <b>NULL</b> indicating a named account not the local system account and the <i>pwszPassword</i> parameter was incorrect for the account specified in the <i>pwszAccount</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
<dt>0x08007000d</dt>
</dl>
</td>
<td width="60%">
The data is invalid. This error is returned if the <i>pwszPassword</i> parameter was <b>NULL</b> or the length of  <i>pwszPassword</i> parameter string was too long.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_ACCOUNT_NAME_NOT_FOUND</b></dt>
<dt>0x80041310</dt>
</dl>
</td>
<td width="60%">
Unable to establish existence of the account specified. This error is returned if the <i>pwszAccount</i> parameter  was  not <b>NULL</b> indicating a named account not the local system account and  the <i>pwszAccount</i> parameter could not be found. 

</td>
</tr>
</table>
 




## -remarks



The <b>SetNetScheduleAccountInformation</b> impersonates the caller. Only members of the local Administrators group on the computer where the schedule account information is being set can successfully execute this function. Note that <b>NULL</b> passwords are not allowed.




## -see-also




<a href="https://msdn.microsoft.com/935de94a-6791-4ea2-ac39-cf71ef7cb726">GetNetScheduleAccountInformation</a>
 

 

