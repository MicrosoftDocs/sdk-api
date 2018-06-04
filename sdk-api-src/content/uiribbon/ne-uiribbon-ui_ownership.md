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

# UI_OWNERSHIP enumeration


## -description


Specifies values that identify the ownership conditions under which an image is created by the Windows Ribbon framework.


## -enum-fields




### -field UI_OWNERSHIP_TRANSFER


			The handle to the bitmap (HBITMAP) is owned by the Ribbon framework 
			through the <a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a> object.
			


### -field UI_OWNERSHIP_COPY


			A copy of the HBITMAP is created by the Ribbon framework through 
			the <a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a> object. The host application still owns the HBITMAP.
			


## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/09eea6ad-c756-4044-b98f-6d6ba87437db">IUIImageFromBitmap::CreateImage</a>
 

 

