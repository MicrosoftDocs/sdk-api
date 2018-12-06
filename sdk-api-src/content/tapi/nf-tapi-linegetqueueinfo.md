---
UID: NF:tapi.lineGetQueueInfo
title: lineGetQueueInfo function
author: windows-sdk-content
description: The lineGetQueueInfo function returns a structure holding the ACD information associated with a particular queue.
old-location: tapi2\linegetqueueinfo.htm
tech.root: tapi
ms.assetid: f7bd6922-a9cd-43ab-96f7-5abf4c6a5b16
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linegetqueueinfo, lineGetQueueInfo, lineGetQueueInfo function [TAPI 2.2], tapi/lineGetQueueInfo, tapi2.linegetqueueinfo"
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
req.unicode-ansi: 
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
 - lineGetQueueInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetQueueInfo function


## -description


The 
<b>lineGetQueueInfo</b> function returns a structure holding the ACD information associated with a particular queue. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETQUEUEINFO.


## -parameters




### -param hLine

Handle to the line device.


### -param dwQueueID

Identifier of the queue whose information is to be retrieved.


### -param lpLineQueueInfo

Pointer to a structure of type 
<a href="https://msdn.microsoft.com/ba49404f-eb84-485f-be27-60760986d489">LINEQUEUEINFO</a>. Upon successful completion of the request, this structure is filled with the queue statistics. Prior to calling 
<b>lineGetQueueInfo</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/ba49404f-eb84-485f-be27-60760986d489">LINEQUEUEINFO</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

