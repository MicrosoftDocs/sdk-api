---
UID: NF:bcrypt.BCryptImportKeyPair
title: BCryptImportKeyPair function
author: windows-sdk-content
description: Imports a public/private key pair from a key BLOB.
old-location: security\bcryptimportkeypair.htm
old-project: SecCNG
ms.assetid: 271fc084-6121-4666-b521-b849c7d7966c
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: BCRYPT_DH_PRIVATE_BLOB, BCRYPT_DH_PUBLIC_BLOB, BCRYPT_DSA_PRIVATE_BLOB, BCRYPT_DSA_PUBLIC_BLOB, BCRYPT_ECCPRIVATE_BLOB, BCRYPT_ECCPUBLIC_BLOB, BCRYPT_NO_KEY_VALIDATION, BCRYPT_PRIVATE_KEY_BLOB, BCRYPT_PUBLIC_KEY_BLOB, BCRYPT_RSAPRIVATE_BLOB, BCRYPT_RSAPUBLIC_BLOB, BCryptImportKeyPair, BCryptImportKeyPair function [Security], LEGACY_DH_PRIVATE_BLOB, LEGACY_DH_PUBLIC_BLOB, LEGACY_DSA_PRIVATE_BLOB, LEGACY_DSA_PUBLIC_BLOB, LEGACY_DSA_V2_PRIVATE_BLOB, LEGACY_RSAPRIVATE_BLOB, LEGACY_RSAPUBLIC_BLOB, bcrypt/BCryptImportKeyPair, security.bcryptimportkeypair
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: HASHALGORITHM_ENUM
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
-	Bcrypt.dll
-	Ksecdd.sys
 - accctrl.h
: 
api_name:
-	BCryptImportKeyPair
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
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
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
---

# BCryptImportKeyPair function


## -description


The <b>BCryptImportKeyPair</b> function imports a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pair</a> from a key <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>. The <a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a> function is used to import a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a> pair.


## -parameters




### -param hAlgorithm [in]

The handle of the algorithm provider to import the key. This handle is obtained by calling the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function.


### -param hImportKey [in, out]

This parameter is not currently used and should be <b>NULL</b>.


### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the type of BLOB that is contained in the <i>pbInput</i> buffer. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PRIVATE_BLOB"></a><a id="bcrypt_dh_private_blob"></a><dl>
<dt><b>BCRYPT_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/6004b2e5-7e06-4108-a0da-472b9b6d5fea">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PUBLIC_BLOB"></a><a id="bcrypt_dh_public_blob"></a><dl>
<dt><b>BCRYPT_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a>. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/6004b2e5-7e06-4108-a0da-472b9b6d5fea">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PRIVATE_BLOB"></a><a id="bcrypt_dsa_private_blob"></a><dl>
<dt><b>BCRYPT_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/3db36170-106e-49c8-9866-e25759bdd7f9">BCRYPT_DSA_KEY_BLOB</a> or <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data. <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PUBLIC_BLOB"></a><a id="bcrypt_dsa_public_blob"></a><dl>
<dt><b>BCRYPT_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public key BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/3db36170-106e-49c8-9866-e25759bdd7f9">BCRYPT_DSA_KEY_BLOB</a> or <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data. <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPRIVATE_BLOB"></a><a id="bcrypt_eccprivate_blob"></a><dl>
<dt><b>BCRYPT_ECCPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">elliptic curve cryptography</a> (ECC) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/e60f6630-e4b0-4f35-a3cf-95dbcb007124">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data. 

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPUBLIC_BLOB"></a><a id="bcrypt_eccpublic_blob"></a><dl>
<dt><b>BCRYPT_ECCPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an ECC public key. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/e60f6630-e4b0-4f35-a3cf-95dbcb007124">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PUBLIC_KEY_BLOB"></a><a id="bcrypt_public_key_blob"></a><dl>
<dt><b>BCRYPT_PUBLIC_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a generic <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> of any type. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="https://msdn.microsoft.com/ae7e8db3-858d-4573-afe1-c9bc14d76480">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PRIVATE_KEY_BLOB"></a><a id="bcrypt_private_key_blob"></a><dl>
<dt><b>BCRYPT_PRIVATE_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a generic private key of any type. The private key does not necessarily contain the public key. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="https://msdn.microsoft.com/ae7e8db3-858d-4573-afe1-c9bc14d76480">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPRIVATE_BLOB"></a><a id="bcrypt_rsaprivate_blob"></a><dl>
<dt><b>BCRYPT_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/bbf3f4b9-5c69-4212-bb23-34bb2c84185c">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPUBLIC_BLOB"></a><a id="bcrypt_rsapublic_blob"></a><dl>
<dt><b>BCRYPT_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public key BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/bbf3f4b9-5c69-4212-bb23-34bb2c84185c">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PUBLIC_BLOB"></a><a id="legacy_dh_public_blob"></a><dl>
<dt><b>LEGACY_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman public key BLOB that was exported by using <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a>. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PRIVATE_BLOB"></a><a id="legacy_dh_private_blob"></a><dl>
<dt><b>LEGACY_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a legacy <a href="https://msdn.microsoft.com/c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1">Diffie-Hellman Version 3 Private Key BLOB</a> that contains a Diffie-Hellman public/private key pair that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PRIVATE_BLOB"></a><a id="legacy_dsa_private_blob"></a><dl>
<dt><b>LEGACY_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public/private key pair BLOB that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PUBLIC_BLOB"></a><a id="legacy_dsa_public_blob"></a><dl>
<dt><b>LEGACY_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public key BLOB that was exported by using CryptoAPI. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_V2_PRIVATE_BLOB"></a><a id="legacy_dsa_v2_private_blob"></a><dl>
<dt><b>LEGACY_DSA_V2_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA version 2 private key in a form that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPRIVATE_BLOB"></a><a id="legacy_rsaprivate_blob"></a><dl>
<dt><b>LEGACY_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public/private key pair BLOB that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPUBLIC_BLOB"></a><a id="legacy_rsapublic_blob"></a><dl>
<dt><b>LEGACY_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public key BLOB that was exported by using CryptoAPI. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
</table>
 


### -param phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> that receives the handle of the imported key. This handle is used in subsequent functions that require a key, such as <a href="https://msdn.microsoft.com/f402ea9e-89ae-4ccc-9591-aa2328287c0e">BCryptSignHash</a>. This handle must be released when it is no longer needed by passing it to the <a href="https://msdn.microsoft.com/98c02e55-6489-4901-8a7a-021baac41965">BCryptDestroyKey</a> function.


### -param pbInput [in]

The address of a buffer that contains the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> to import. The <i>cbInput</i> parameter contains the size of this buffer. The <i>pszBlobType</i> parameter specifies the type of key BLOB this buffer contains.


### -param cbInput [in]

The size, in bytes, of the <i>pbInput</i> buffer.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_NO_KEY_VALIDATION"></a><a id="bcrypt_no_key_validation"></a><dl>
<dt><b>BCRYPT_NO_KEY_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
Do not validate the public portion of the key pair.

</td>
</tr>
</table>
 


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The algorithm handle in the <i>hAlgorithm</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The algorithm provider specified by the <i>hAlgorithm</i> parameter does not support the BLOB type specified by the <i>pszBlobType</i> parameter.

</td>
</tr>
</table>
 




## -remarks



Depending on what processor modes a provider supports, <b>BCryptImportKeyPair</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptImportKeyPair</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/98c02e55-6489-4901-8a7a-021baac41965">BCryptDestroyKey</a>



<a href="https://msdn.microsoft.com/a5d73143-c1d6-43b3-a724-7e27c68a5ade">BCryptExportKey</a>



<a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a>
 

 

