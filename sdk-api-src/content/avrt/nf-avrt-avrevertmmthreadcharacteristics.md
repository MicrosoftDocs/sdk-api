---
UID: NF:avrt.AvRevertMmThreadCharacteristics
title: AvRevertMmThreadCharacteristics function
author: windows-sdk-content
description: Indicates that a thread is no longer performing work associated with the specified task.
old-location: base\avrevertmmthreadcharacteristics.htm
old-project: ProcThread
ms.assetid: 2ae0d34c-3819-46fa-9779-5de8a57e5281
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: AvRevertMmThreadCharacteristics, AvRevertMmThreadCharacteristics function, avrt/AvRevertMmThreadCharacteristics, base.avrevertmmthreadcharacteristics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: AVRF_HEAP_ALLOCATION, *PAVRF_HEAP_ALLOCATION
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
-	Avrt.dll
 - accctrl.h
: 
api_name:
-	AvRevertMmThreadCharacteristics
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
req.lib: Avrt.lib
req.dll: Avrt.dll
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
---

# AvRevertMmThreadCharacteristics function


## -description


Indicates that a thread is no longer performing work associated with the specified task.


## -parameters




### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> or <a href="https://msdn.microsoft.com/d8137b53-b1fd-4c25-909a-d0ed671848df">AvSetMmMaxThreadCharacteristics</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function must be called from the same thread that called the <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> or <a href="https://msdn.microsoft.com/d8137b53-b1fd-4c25-909a-d0ed671848df">AvSetMmMaxThreadCharacteristics</a> function to create the handle. Otherwise, the function will fail.




## -see-also




<a href="https://msdn.microsoft.com/a7169938-1c72-4c4c-881a-cb08ad6182c7">Multimedia Class Scheduler Service</a>
 

 

