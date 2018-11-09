---
UID: NF:tapi.lineGetAddressStatusA
title: lineGetAddressStatusA function
author: windows-sdk-content
description: The lineGetAddressStatus function allows an application to query the specified address for its current status.
old-location: tapi2\linegetaddressstatus.htm
tech.root: tapi
ms.assetid: 8d747aa5-05cc-4426-9d46-24bce6b4af26
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_tapi2_linegetaddressstatus, lineGetAddressStatus, lineGetAddressStatus function [TAPI 2.2], lineGetAddressStatusA, lineGetAddressStatusW, tapi/lineGetAddressStatus, tapi/lineGetAddressStatusA, tapi/lineGetAddressStatusW, tapi2.linegetaddressstatus"
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
req.unicode-ansi: lineGetAddressStatusW (Unicode) and lineGetAddressStatusA (ANSI)
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
 - lineGetAddressStatus
 - lineGetAddressStatusA
 - lineGetAddressStatusW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetAddressStatusA function


## -description


The 
<b>lineGetAddressStatus</b> function allows an application to query the specified address for its current status.


## -parameters




### -param hLine

Handle to the open line device.


### -param dwAddressID

Address on the given open line device. This is the address to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param lpAddressStatus

Pointer to a variably sized data structure of type 
<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a>. Prior to calling 
<b>lineGetAddressStatus</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

