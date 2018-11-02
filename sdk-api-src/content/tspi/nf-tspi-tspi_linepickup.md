---
UID: NF:tspi.TSPI_linePickup
title: TSPI_linePickup function
author: windows-sdk-content
description: The TSPI_linePickup function picks up a call alerting at the specified destination address and returns a call handle for the picked-up call.
old-location: tspi\tspi_linepickup.htm
tech.root: tapi
ms.assetid: 97ab8896-3794-4de2-a1af-41025d2b6b17
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TSPI_linePickup, TSPI_linePickup function [TAPI 2.2], _tspi_tspi_linepickup, tspi.tspi_linepickup, tspi/TSPI_linePickup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_linePickup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_linePickup function


## -description


The 
<b>TSPI_linePickup</b> function picks up a call alerting at the specified destination address and returns a call handle for the picked-up call. If invoked with <b>NULL</b> for the <i>lpszDestAddress</i> parameter, a group pickup is performed. If required by the device capabilities, <i>lpszGroupID</i> specifies the group identifier to which the alerting station belongs.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdLine

The handle to the line on which a call is to be picked up.


### -param dwAddressID

The address on <i>hdLine</i> at which the pickup is to be originated. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param htCall

The TAPI handle to the new call. The service provider must save this and use it in all subsequent calls to the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> procedure reporting events on the call.


### -param lphdCall

A pointer to an 
<a href="https://msdn.microsoft.com/8bb1c3fe-a3de-4299-bc15-58321c5da549">HDRVCALL</a> representing the service provider's identifier for the call. The service provider must fill this location with its handle for the call before this procedure returns. This handle is ignored by TAPI if the function results in an error.


### -param lpszDestAddress

A pointer to a <b>null</b>-terminated Unicode string that contains the address whose call is to be picked up. The address is standard link format.


### -param lpszGroupID

A pointer to a <b>null</b>-terminated Unicode string containing the group identifier to which the alerting station belongs. This parameter is required on some switches to pick up calls outside of the current pickup group. 




<div class="alert"><b>Note</b>  <i>lpszGroupID</i> can be specified by itself with a <b>NULL</b> pointer for <i>lpszDestAddress</i>. Alternatively, <i>lpszGroupID</i> can be specified in addition to <i>lpszDestAddress</i>, if required by the device. It can also be <b>NULL</b> itself.</div>
<div> </div>

## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_INVALGROUPID, LINEERR_RESOURCEUNAVAIL.




## -remarks



When a call has been picked up successfully, the service provider notifies TAPI with the 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> message about call state changes. The 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure supplies information about the call that was picked up. It lists the reason for the call as <i>pickup</i>. This structure is available by calling 
<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>.

The service provider sets LINEADDRCAPFLAGS_PICKUPCALLWAIT to <b>TRUE</b> in the 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> structure if 
<b>TSPI_linePickup</b> can be used to pick up a call for which the user has audibly detected the call-waiting signal, but for which the provider is unable to perform the detection. This gives the user a mechanism to answer a waiting call even though the service provider was unable to detect the call-waiting signal. When 
<b>TSPI_linePickup</b> is being used to pick up a call-waiting call, both <i>lpszDestAddress</i> and <i>lpszGroupID</i> pointer parameters are <b>NULL</b>. The service provider creates a new call handle for the waiting call and passes that handle to the user in <i>lphdCall</i>. The <i>dwAddressID</i> parameter is most often zero (particularly in single-line residential cases).

Once 
<b>TSPI_linePickup</b> is used to pick up the second call, 
<a href="https://msdn.microsoft.com/9ecd6a63-e906-483b-b404-28797d259149">TSPI_lineSwapHold</a> can be used to toggle between them. 
<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a> can be used to drop one (and toggle to the other), and so forth. If the user wants to drop the current call and pick up the second call, they call 
<b>TSPI_lineDrop</b> when they get the call-waiting beep, wait for the second call to ring, and then call 
<a href="https://msdn.microsoft.com/efd4d7f8-bf81-46c4-b51b-516036e9baef">TSPI_lineAnswer</a> on the new call handle. The service provider sets the LINEADDRFEATURE_PICKUP flag in the <b>dwAddressFeatures</b> member in 
<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a> to indicate when pickup is actually possible.

This function differs from the corresponding TAPI function in that it follows the TSPI model for beginning the lifetime of a call. TAPI and the service provider exchange opaque handles representing the call with one another. In addition, the service provider is permitted to do callbacks for the new call before it returns from this procedure. In any case, the service provider must also treat the handle it returned as "not yet valid" until after the matching 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> message reports success. In other words, it must not issue any 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> messages for the new call or include it in call counts in messages or status data structures for the line.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a>



<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>



<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/efd4d7f8-bf81-46c4-b51b-516036e9baef">TSPI_lineAnswer</a>



<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a>



<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/7124ef73-148f-41df-afd6-ebfa29d5cf1c">TSPI_lineGetCallStatus</a>



<a href="https://msdn.microsoft.com/9ecd6a63-e906-483b-b404-28797d259149">TSPI_lineSwapHold</a>
 

 

