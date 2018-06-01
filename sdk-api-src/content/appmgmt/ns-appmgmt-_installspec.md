---
UID: NS:appmgmt._INSTALLSPEC
title: "_INSTALLSPEC"
author: windows-sdk-content
description: The INSTALLSPEC structure specifies a group policy application by its user-friendly name and group policy GUID or by its file name extension. The Spec member of the INSTALLDATA structure provides this information to the InstallApplication function.
old-location: policy\installspec_union.htm
old-project: Policy
ms.assetid: e9c1b943-9cb0-480f-8ab7-0f439087216a
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: INSTALLSPEC, INSTALLSPEC union [Group Policy], _INSTALLSPEC, appmgmt/INSTALLSPEC, policy.installspec_union
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: appmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: INSTALLSPEC
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	HeaderDef
 - HeaderDef
: 
api_location:
-	Appmgmt.h
 - accctrl.h
: 
api_name:
-	INSTALLSPEC
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
---

# _INSTALLSPEC structure


## -description


The <b>INSTALLSPEC</b> structure specifies a group policy application by its user-friendly name and group policy GUID or by its file name extension. The <b>Spec</b> member of the <a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a>  structure provides this information to the <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a> function.


## -struct-fields




### -field AppName

Structure that contains the following members.


### -field AppName.Name

The user-friendly name of the application as it appears in <b>Add or Remove Programs</b> and the <a href="https://msdn.microsoft.com/0fc85897-c96d-457a-a189-6fa0165eb11b">Group Policy Object Editor</a>. You can obtain the name by calling <a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a>.


### -field AppName.GPOId

The <b>GUID</b> for the group policy object in which the application exists. You can obtain the group policy object <b>GUID</b> by calling <a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a>.


### -field FileExt

The file name extension, such as .jpg,  of the application to be installed.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a> fails if the <b>Type</b> member of <a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a> equals <b>FILEEXT</b> and there is no application deployed to the user with this file name extension.</div>
<div> </div>

### -field ProgId

 


### -field COMClass

 


### -field COMClass.Clsid

 


### -field COMClass.ClsCtx

 




#### - Reserved1

This parameter is reserved and should not be used.


#### - Reserved2

Structure that contains the following members.



#### Reserved1

This parameter is reserved and should not be used.



#### Reserved2

This parameter is reserved and should not be used.


## -see-also




<a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a>



<a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>



<a href="https://msdn.microsoft.com/d45494e2-d86e-4d94-a158-4024eacf46a2">UninstallApplication</a>
 

 

