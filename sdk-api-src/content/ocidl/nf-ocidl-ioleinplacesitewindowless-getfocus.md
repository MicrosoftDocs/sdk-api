---
UID: NF:ocidl.IOleInPlaceSiteWindowless.GetFocus
title: IOleInPlaceSiteWindowless::GetFocus
author: windows-sdk-content
description: Called by an in-place active, windowless object to determine whether it still has the keyboard focus.
old-location: com\ioleinplacesitewindowless_getfocus.htm
old-project: com
ms.assetid: 282f350c-d196-40c2-880f-55f28dc48f2b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetFocus, GetFocus method [COM], GetFocus method [COM],IOleInPlaceSiteWindowless interface, IOleInPlaceSiteWindowless interface [COM],GetFocus method, IOleInPlaceSiteWindowless.GetFocus, IOleInPlaceSiteWindowless::GetFocus, _ole_ioleinplacesitewindowless_getfocus, com.ioleinplacesitewindowless_getfocus, ocidl/IOleInPlaceSiteWindowless::GetFocus
ms.prod: windows
ms.technology: windows-sdk
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
-	IOleInPlaceSiteWindowless.GetFocus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleInPlaceSiteWindowless::GetFocus


## -description


Called by an in-place active, windowless object to determine whether it still has the keyboard focus.


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
The object does not currently have the keyboard focus.

</td>
</tr>
</table>
 




## -remarks



A windowless object calls this method to find out if it currently has the focus or not. As an alternative to calling this method, the object can cache information about whether it has the keyboard focus or not.




## -see-also




<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>
 

 

