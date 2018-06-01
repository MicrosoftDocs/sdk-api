---
UID: NN:audiopolicy.IAudioSessionEnumerator
title: IAudioSessionEnumerator
author: windows-sdk-content
description: The IAudioSessionEnumerator interface enumerates audio sessions on an audio device.
old-location: coreaudio\iaudiosessionenumerator.htm
old-project: CoreAudio
ms.assetid: a7976d13-3391-4747-b83a-cfb9407b34f2
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioSessionEnumerator, IAudioSessionEnumerator interface [Core Audio], IAudioSessionEnumerator interface [Core Audio],described, audiopolicy/IAudioSessionEnumerator, coreaudio.iaudiosessionenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	COM
 - HeaderDef
: 
api_location:
-	audiopolicy.h
 - accctrl.h
: 
api_name:
-	IAudioSessionEnumerator
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
---

# IAudioSessionEnumerator interface


## -description


The <b>IAudioSessionEnumerator</b> interface enumerates audio sessions on an audio device. To get a reference to the <b>IAudioSessionEnumerator</b> interface of the session enumerator object, the application must call <a href="https://msdn.microsoft.com/68166fc1-af27-4251-8e18-be23d205b567">IAudioSessionManager2::GetSessionEnumerator</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioSessionEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSessionEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1fbfbf5-a79b-40bc-97c7-a76a181bbfec">
        GetCount</a>
</td>
<td align="left" width="63%">
Gets the total number of audio sessions that are open on the audio device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45b7af16-aca0-49f8-b977-f7e4f1885687">GetSession</a>
</td>
<td align="left" width="63%">
Gets the audio session specified by an audio session number. 

</td>
</tr>
</table> 


## -remarks



If an application wants to be  notified when new sessions are created, it must register its implementation of  <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> with the session manager.  Upon successful registration, the session manager sends create-session notifications to the application in the form of callbacks. These notifications contain a reference to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointer of the newly created session. 

The session enumerator maintains a list of current sessions by holding references to each session's <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointer. However, the session enumerator might not be aware of the new sessions that are reported through <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a>. In that case, the application would have access to only a partial list of sessions. This might occur if the <b>IAudioSessionControl</b> pointer (in the callback) is released before the session enumerator is initialized. Therefore,    if an application wants a complete set of sessions for the audio endpoint, the application should maintain its own list. 

The application must perform the following steps to receive session notifications and manage a list of current sessions.

<ol>
<li>Initialize COM with the Multithreaded Apartment (MTA) model by calling <code>CoInitializeEx(NULL, COINIT_MULTITHREADED)</code> in a non-UI thread. If MTA is not initialized, the application does not receive session notifications from the session manager.  <div class="alert"><b>Note</b>  Threads that run the user interface of an application should be initialized with the apartment threading model.</div>
<div> </div>
</li>
<li>Activate an <a href="https://msdn.microsoft.com/476dac90-d0c4-499c-973e-33ea55546659">IAudioSessionManager2</a> interface from the audio endpoint device. Call <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> with parameter <i>iid</i> set to <b>IID_IAudioSessionManager2</b>. This call receives a reference to the session manager's <b>IAudioSessionManager2</b> interface in the <i>ppInterface</i> parameter.  </li>
<li>Implement the <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface to provide the callback behavior.</li>
<li>Call <a href="https://msdn.microsoft.com/cff43da7-70b2-4887-8a6c-6100cf7d696e">IAudioSessionManager2::RegisterSessionNotification</a> to register the application's implementation of  <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a>.</li>
<li>Create and initialize the session enumerator object by calling <a href="https://msdn.microsoft.com/68166fc1-af27-4251-8e18-be23d205b567">IAudioSessionManager2::GetSessionEnumerator</a>. This method generates a list of current sessions available for the endpoint and adds the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointers for  each session in the list, if they are not already present.</li>
<li>Use the <b>IAudioSessionEnumerator</b> interface returned in the previous step to retrieve and enumerate the list of sessions. The session control for each session can be retrieved by calling <a href="https://msdn.microsoft.com/45b7af16-aca0-49f8-b977-f7e4f1885687">IAudioSessionEnumerator::GetSession</a>. Make sure you call <b>AddRef</b> for each session control to maintain the reference count.</li>
<li>When the application gets a create-session notification, add  the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointer of the new session (received in <a href="https://msdn.microsoft.com/03f22e06-f446-4c57-a955-3d12deec4152">IAudioSessionNotification::OnSessionCreated</a>)  to the list of existing sessions. </li>
</ol>
Because the application maintains this list of sessions and manages the lifetime of the session based on the application's requirements, there is no expiration mechanism enforced by the audio system on the session control objects.

A session control is valid as long as the application has a reference to the session control in the list.  


#### Examples

The following example code shows how to create the session enumerator object and then enumerate sessions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT EnumSessions(IAudioSessionManager2* pSessionManager)
{
    if (!pSessionManager)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;
    
    int cbSessionCount = 0;
    LPWSTR pswSession = NULL;
    
    IAudioSessionEnumerator* pSessionList = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    
    // Get the current list of sessions.
    CHECK_HR( hr = pSessionManager-&gt;GetSessionEnumerator(&amp;pSessionList));
    
    // Get the session count.
    CHECK_HR( hr = pSessionList-&gt;GetCount(&amp;cbSessionCount));

    for (int index = 0 ; index &lt; cbSessionCount ; index++)
    {
        CoTaskMemFree(pswSession);
        SAFE_RELEASE(pSessionControl);
        
        // Get the &lt;n&gt;th session.
        CHECK_HR(hr = pSessionList-&gt;GetSession(index, &amp;pSessionControl));

        CHECK_HR(hr = pSessionControl-&gt;GetDisplayName(&amp;pswSession));

        wprintf_s(L"Session Name: %s\n", pswSession);
    }

done:
    CoTaskMemFree(pswSession);
    SAFE_RELEASE(pSessionControl);
    SAFE_RELEASE(pSessionList);

    return hr;

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

