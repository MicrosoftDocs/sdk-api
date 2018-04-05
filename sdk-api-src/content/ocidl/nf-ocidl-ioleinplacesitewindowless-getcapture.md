---
UID: NF:ocidl.IOleInPlaceSiteWindowless.GetCapture
title: IOleInPlaceSiteWindowless::GetCapture method
author: windows-driver-content
description: Called by an in-place active, windowless object to determine whether it still has the mouse capture.
old-location: com\ioleinplacesitewindowless_getcapture.htm
old-project: com
ms.assetid: adbe9c66-d716-4489-b705-43a5317c7646
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCapture method [COM], GetCapture method [COM], IOleInPlaceSiteWindowless interface, GetCapture,IOleInPlaceSiteWindowless.GetCapture, IOleInPlaceSiteWindowless, IOleInPlaceSiteWindowless interface [COM], GetCapture method, IOleInPlaceSiteWindowless::GetCapture, _ole_ioleinplacesitewindowless_getcapture, com.ioleinplacesitewindowless_getcapture, ocidl/IOleInPlaceSiteWindowless::GetCapture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IOleInPlaceSiteWindowless.GetCapture
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOleInPlaceSiteWindowless::GetCapture method


## -description


Called by an in-place active, windowless object to determine whether it still has the mouse capture.


## -parameters






## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object does not currently have the mouse capture.

</td>
</tr>
</table>
 




## -remarks



As an alternative to calling this method, the object can cache information about whether it has the mouse capture.




## -see-also




<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>
 

 

