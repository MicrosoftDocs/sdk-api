---
UID: NF:tapi.lineGetGroupListW
title: lineGetGroupListW function (tapi.h)
description: The lineGetGroupList function returns a list of ACD groups available on the ACD system.
old-location: tapi2\linegetgrouplist.htm
tech.root: Tapi
ms.assetid: 3e1d63e2-f87d-41ed-92ba-fe3bbdade8d3
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetgrouplist, lineGetGroupList, lineGetGroupList function [TAPI 2.2], lineGetGroupListA, lineGetGroupListW, tapi/lineGetGroupList, tapi/lineGetGroupListA, tapi/lineGetGroupListW, tapi2.linegetgrouplist
f1_keywords:
- tapi/lineGetGroupList
dev_langs:
- c++
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetGroupListW (Unicode) and lineGetGroupListA (ANSI)
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
- lineGetGroupList
- lineGetGroupListA
- lineGetGroupListW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineGetGroupListW function


## -description


The 
<b>lineGetGroupList</b> function returns a list of ACD groups available on the ACD system. It generates a 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type <b>LINEPROXYREQUEST_GETGROUPLIST</b>.


## -parameters




### -param hLine

Handle to the line device.


### -param lpGroupList

Pointer to a variably sized structure of type 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a>. Upon successful completion of the request, this structure is filled with a list of the available ACD groups. Prior to calling the 
<b>lineGetGroupList</b> function, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>
 

 

