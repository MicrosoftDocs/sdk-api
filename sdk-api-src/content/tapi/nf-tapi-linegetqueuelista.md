---
UID: NF:tapi.lineGetQueueListA
title: lineGetQueueListA function
author: windows-sdk-content
description: The lineGetQueueList function returns a list of queues associated with a particular ACD Group.
old-location: tapi2\linegetqueuelist.htm
tech.root: Tapi
ms.assetid: 3921ab24-c9c8-4068-a885-e55759f04076
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_tapi2_linegetqueuelist, lineGetQueueList, lineGetQueueList function [TAPI 2.2], lineGetQueueListA, lineGetQueueListW, tapi/lineGetQueueList, tapi/lineGetQueueListA, tapi/lineGetQueueListW, tapi2.linegetqueuelist"
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
req.unicode-ansi: lineGetQueueListW (Unicode) and lineGetQueueListA (ANSI)
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
 - lineGetQueueList
 - lineGetQueueListA
 - lineGetQueueListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetQueueListA function


## -description


The 
<b>lineGetQueueList</b> function returns a list of queues associated with a particular ACD Group. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETQUEUELIST.


## -parameters




### -param hLine

Handle to the line device.


### -param lpGroupID

Pointer to GUID that identifies the group for which the list of queues is requested.


### -param lpQueueList

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a>. Upon successful completion of the request, this structure is filled with a list of queues. Prior to calling 
<b>lineGetQueueList</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

