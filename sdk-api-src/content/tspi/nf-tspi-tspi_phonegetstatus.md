---
UID: NF:tspi.TSPI_phoneGetStatus
title: TSPI_phoneGetStatus function (tspi.h)
description: The TSPI_phoneGetStatus function queries the specified open phone device for its overall status.
helpviewer_keywords: ["TSPI_phoneGetStatus","TSPI_phoneGetStatus function [TAPI 2.2]","_tspi_tspi_phonegetstatus","tspi.tspi_phonegetstatus","tspi/TSPI_phoneGetStatus"]
old-location: tspi\tspi_phonegetstatus.htm
tech.root: tapi3
ms.assetid: 92cf7299-2e1f-42ce-abf7-2824d993bd59
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetStatus, TSPI_phoneGetStatus function [TAPI 2.2], _tspi_tspi_phonegetstatus, tspi.tspi_phonegetstatus, tspi/TSPI_phoneGetStatus
req.header: tspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_phoneGetStatus
 - tspi/TSPI_phoneGetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneGetStatus
---

# TSPI_phoneGetStatus function


## -description

The 
<b>TSPI_phoneGetStatus</b> function queries the specified open phone device for its overall status.

## -parameters

### -param hdPhone

The handle to the phone to be queried.

### -param lpPhoneStatus

A pointer to a variably sized data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a>, into which the service provider writes information about the phone's status. Prior to calling 
<b>TSPI_phoneGetStatus</b>, the application sets the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_RESOURCEUNAVAIL.

## -remarks

The following table indicates which members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a> data structure are filled in by TAPI and which members are filled in by the service provider. The service provider must not overwrite the values filled in by TAPI.

<table>
<tr>
<th>Member</th>
<th>TAPI</th>
<th>Service provider</th>
</tr>
<tr>
<td><b>dwTotalSize;</b></td>
<td>X</td>
<td> </td>
</tr>
<tr>
<td><b>dwNeededSize;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwUsedSize;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwStatusFlags;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwNumOwners;</b></td>
<td>X</td>
<td> </td>
</tr>
<tr>
<td><b>dwNumMonitors;</b></td>
<td>X</td>
<td> </td>
</tr>
<tr>
<td><b>dwRingMode;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwRingVolume;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwHandsetHookSwitchMode;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwHandsetVolume;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwHandsetGain;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwSpeakerHookSwitchMode;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwSpeakerVolume;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwSpeakerGain;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwHeadsetHookSwitchMode;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwHeadsetVolume;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwHeadsetGain;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwDisplaySize;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwDisplayOffset;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwLampModesSize;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwLampModesOffset;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwOwnerNameSize;</b></td>
<td>X</td>
<td> </td>
</tr>
<tr>
<td><b>dwOwnerNameOffset;</b></td>
<td>X</td>
<td> </td>
</tr>
<tr>
<td><b>dwDevSpecificSize;</b></td>
<td> </td>
<td>X</td>
</tr>
<tr>
<td><b>dwDevSpecificOffset;</b></td>
<td> </td>
<td>X</td>
</tr>
</table>
 

TAPI can use this function to determine the current state of an open phone device. The status information describes information about the phone device's hookswitch devices, ringer, volume, display, and lamps of the open phone.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725262(v=vs.85)">PHONE_STATE</a>