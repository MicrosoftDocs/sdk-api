---
UID: NS:winbio_types._WINBIO_EVENT
title: "_WINBIO_EVENT"
author: windows-driver-content
description: Contains status information sent to the callback routine when an event notice is raised.
old-location: secbiomet\winbio_event.htm
old-project: SecBioMet
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_EVENT, PWINBIO_EVENT, PWINBIO_EVENT structure pointer [Windows Biometric Framework API], WINBIO_EVENT, WINBIO_EVENT structure [Windows Biometric Framework API], WINBIO_EVENT_FP_UNCLAIMED, WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY, _WINBIO_EVENT, secbiomet.winbio_event, winbio_types/PWINBIO_EVENT, winbio_types/WINBIO_EVENT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_types.h
req.include-header: Winbio.h
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
req.typenames: WINBIO_EVENT, *PWINBIO_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_EVENT structure


## -description


The <b>WINBIO_EVENT</b> structure contains status information sent to the callback routine when an event notice is raised.


## -struct-fields




### -field Parameters


### -field Parameters.Unclaimed

Structure returned for biometric sample capture.


### -field Parameters.Unclaimed.UnitId

The biometric unit that generated the sample.


### -field Parameters.Unclaimed.RejectDetail

A <b>ULONG</b> value that contains additional information regarding failure to capture a biometric sample. If a capture succeeded, this parameter is set to zero. The following values are defined for fingerprint capture:

<ul>
<li>WINBIO_FP_TOO_HIGH</li>
<li>WINBIO_FP_TOO_LOW</li>
<li>WINBIO_FP_TOO_LEFT</li>
<li>WINBIO_FP_TOO_RIGHT</li>
<li>WINBIO_FP_TOO_FAST</li>
<li>WINBIO_FP_TOO_SLOW</li>
<li>WINBIO_FP_POOR_QUALITY</li>
<li>WINBIO_FP_TOO_SKEWED</li>
<li>WINBIO_FP_TOO_SHORT</li>
<li>WINBIO_FP_MERGE_FAILURE</li>
</ul>

### -field Parameters.UnclaimedIdentify

Structure returned for biometric capture and identification. Identification determines whether a sample can be associated with an existing biometric template.




### -field Parameters.UnclaimedIdentify.UnitId

The biometric unit that generated the sample.


### -field Parameters.UnclaimedIdentify.Identity

A  <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that contains the GUID or SID of the user providing the biometric sample.


### -field Parameters.UnclaimedIdentify.SubFactor

A <a href="https://msdn.microsoft.com/019569A9-6184-4E75-9B82-C98F4F45F61A">WINBIO_BIOMETRIC_SUBTYPE</a> value that specifies the sub-factor associated with a biometric sample. The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.

<ul>
<li>WINBIO_ANSI_381_POS_UNKNOWN</li>
<li>WINBIO_ANSI_381_POS_RH_THUMB</li>
<li>WINBIO_ANSI_381_POS_RH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_LITTLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_THUMB</li>
<li>WINBIO_ANSI_381_POS_LH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_LITTLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_FOUR_FINGERS</li>
<li>WINBIO_ANSI_381_POS_LH_FOUR_FINGERS</li>
<li>WINBIO_ANSI_381_POS_TWO_THUMBS</li>
</ul>
<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>SubFactor</i> value. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

</div>
<div> </div>

### -field Parameters.UnclaimedIdentify.RejectDetail

A <b>ULONG</b> value that contains additional information about the failure to capture a biometric sample. If the capture succeeded, this parameter is set to zero. The following values are defined for fingerprint capture:

<ul>
<li>WINBIO_FP_TOO_HIGH</li>
<li>WINBIO_FP_TOO_LOW</li>
<li>WINBIO_FP_TOO_LEFT</li>
<li>WINBIO_FP_TOO_RIGHT</li>
<li>WINBIO_FP_TOO_FAST</li>
<li>WINBIO_FP_TOO_SLOW</li>
<li>WINBIO_FP_POOR_QUALITY</li>
<li>WINBIO_FP_TOO_SKEWED</li>
<li>WINBIO_FP_TOO_SHORT</li>
<li>WINBIO_FP_MERGE_FAILURE</li>
</ul>

### -field Parameters.Error

Structure that identifies the success or failure of the operation being monitored.


### -field Parameters.Error.ErrorCode

<b>HRESULT</b> value that contains S_OK or an error code that resulted from computations performed by the Windows Biometric Framework.


### -field Type

A value that specifies the type of service provider event notice raised. The only provider currently supported is the fingerprint sensor. This sensor supports the following flags.



###### )



###### )


## -remarks



Call the <a href="https://msdn.microsoft.com/408291ca-66fe-4f4a-8f6e-3a1b60eb2d15">WinBioRegisterEventMonitor</a> function to register a callback routine to receive event notifications from the Windows Biometric Framework. The callback is a custom function that you must define for your application.




## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/408291ca-66fe-4f4a-8f6e-3a1b60eb2d15">WinBioRegisterEventMonitor</a>
 

 

