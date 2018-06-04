---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CachedBitmap::GetLastStatus


## -description


The <b>CachedBitmap::GetLastStatus</b> method returns a value that indicates whether this 
			<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object was constructed successfully.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If this 
						<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object was constructed successfully, the 
						<b>CachedBitmap::GetLastStatus</b> method returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If this 
						<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object was not constructed successfully, the <b>CachedBitmap::GetLastStatus</b> method returns an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration that indicates the nature of the failure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/42e2b664-197c-4c54-9220-b6231d6439d0">Using a Cached Bitmap to Improve Performance</a>
 

 

