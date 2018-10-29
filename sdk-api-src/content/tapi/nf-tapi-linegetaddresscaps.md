---
UID: NF:tapi.lineGetAddressCaps
title: lineGetAddressCaps function
author: windows-sdk-content
description: The lineGetAddressCaps function queries the specified address on the specified line device to determine its telephony capabilities.
old-location: tapi2\linegetaddresscaps.htm
tech.root: Tapi
ms.assetid: 08cdea8a-5b36-428c-b90f-8741ae5f3205
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_tapi2_linegetaddresscaps, lineGetAddressCaps, lineGetAddressCaps function [TAPI 2.2], lineGetAddressCapsA, lineGetAddressCapsW, tapi/lineGetAddressCaps, tapi/lineGetAddressCapsA, tapi/lineGetAddressCapsW, tapi2.linegetaddresscaps"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAddressCapsW (Unicode) and lineGetAddressCapsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetAddressCaps
 - lineGetAddressCapsA
 - lineGetAddressCapsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetAddressCaps function


## -description


The 
<b>lineGetAddressCaps</b> function queries the specified address on the specified line device to determine its telephony capabilities.


## -parameters




### -param hLineApp

Handle to the application's registration with TAPI.


### -param dwDeviceID

Line device containing the address to be queried.


### -param dwAddressID

Address on the given line device whose capabilities are to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param dwAPIVersion

Version number of the Telephony API to be used. The high-order word contains the major version number; the low-order word contains the minor version number. This number is obtained by 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>.


### -param dwExtVersion

Version number of the service provider-specific extensions to be used. This number can be set to zero if no device-specific extensions are to be used. Otherwise, the high-order word contains the major version number; and the low-order word contains the minor version number.


### -param lpAddressCaps

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>. Upon successful completion of the request, this structure is filled with address capabilities information. Prior to calling 
<b>lineGetAddressCaps</b>, the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NOMEM, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONFAILED, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALAPPHANDLE, LINEERR_UNINITIALIZED, LINEERR_INVALPOINTER, LINEERR_OPERATIONUNAVAIL, LINEERR_NODRIVER, LINEERR_NODEVICE.




## -remarks



Valid address identifiers range from zero to one less than the number of addresses returned by 
<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a>. The version number to be supplied is the version number that was returned as part of the line's device capabilities by 
<b>lineGetDevCaps</b>.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 

