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

# IUIImage::GetBitmap


## -description


Retrieves a bitmap to display as an icon in the ribbon and context popup UI of the Windows Ribbon framework.


## -parameters




### -param bitmap [out]

Type: <b>HBITMAP*</b>

When this method returns, contains a pointer to the handle to the requested bitmap.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IUIImage::GetBitmap</b> is called on image property callback triggered by <a href="https://msdn.microsoft.com/6f6f6815-5523-42d9-a6b2-a21dd26756c0">InvalidateUICommand</a>. 




## -see-also




<a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a>



<a href="https://msdn.microsoft.com/f2b98d96-895e-40aa-9969-98bf1c0c8e5f">IUIImageFromBitmap</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

