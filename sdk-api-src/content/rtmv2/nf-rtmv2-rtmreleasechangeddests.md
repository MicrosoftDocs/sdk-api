---
UID: NF:rtmv2.RtmReleaseChangedDests
title: RtmReleaseChangedDests function
author: windows-sdk-content
description: The RtmReleaseChangedDests function releases the changed destination handles.
old-location: rras\rtmreleasechangeddests.htm
tech.root: rras
ms.assetid: 542cb23f-81c2-4b29-b049-ebb5827b1d62
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtmReleaseChangedDests, RtmReleaseChangedDests function [RAS], _rtmv2ref_rtmreleasechangeddests, rras.rtmreleasechangeddests, rtmv2/RtmReleaseChangedDests
ms.topic: function
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmReleaseChangedDests
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmReleaseChangedDests function


## -description


The 
<b>RtmReleaseChangedDests</b> function releases the changed destination handles.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NotifyHandle [in]

Handle to a change notification, obtained from a previous call to 
<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>.


### -param NumDests [in]

Specifies the number of destinations in <i>ChangedDests</i>.


### -param ChangedDests [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structures to release. The changed destinations were obtained from a prior call to 
<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



Always use this function to release changed 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structures obtained from a call to 
<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>.

The 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structure is a variable-sized structure. If a destination contains information for more than one view, the size of 
<b>RTM_DEST_INFO</b> increases for each view. Use the 
<a href="https://msdn.microsoft.com/faad2b79-dcd0-47e7-95ab-05f6bad36650">RTM_SIZE_OF_DEST_INFO</a> macro to determine how large a <i>ChangedDests</i> buffer to allocate before calling this function.




## -see-also




<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>



<a href="https://msdn.microsoft.com/fafe465a-6c89-45b0-83a9-f08d1d9546c6">RtmGetChangeStatus</a>



<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>



<a href="https://msdn.microsoft.com/9e0b4311-deba-45d6-b1c2-a1b661f25d0f">RtmIgnoreChangedDests</a>



<a href="https://msdn.microsoft.com/bde390fe-3ada-48d3-b9aa-b4bb56228eac">RtmIsMarkedForChangeNotification</a>



<a href="https://msdn.microsoft.com/b7db8664-2775-4f96-8e5b-5062a8abcfe0">RtmMarkDestForChangeNotification</a>
 

 

