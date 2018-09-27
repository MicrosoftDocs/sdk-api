---
UID: NF:tapi.lineGetGroupListA
title: lineGetGroupListA function
author: windows-sdk-content
description: The lineGetGroupList function returns a list of ACD groups available on the ACD system.
old-location: tapi2\linegetgrouplist.htm
tech.root: tapi
ms.assetid: 3e1d63e2-f87d-41ed-92ba-fe3bbdade8d3
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "_tapi2_linegetgrouplist, lineGetGroupList, lineGetGroupList function [TAPI 2.2], lineGetGroupListA, lineGetGroupListW, tapi/lineGetGroupList, tapi/lineGetGroupListA, tapi/lineGetGroupListW, tapi2.linegetgrouplist"
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetGroupListA function


## -description


The 
<b>lineGetGroupList</b> function returns a list of ACD groups available on the ACD system. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type <b>LINEPROXYREQUEST_GETGROUPLIST</b>.


## -parameters




### -param hLine

Handle to the line device.


### -param lpGroupList

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>. Upon successful completion of the request, this structure is filled with a list of the available ACD groups. Prior to calling the 
<b>lineGetGroupList</b> function, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

