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

# IDragSourceHelper::InitializeFromBitmap


## -description


Initializes the drag-image manager for a windowless control.


## -parameters




### -param pshdi [in]

Type: <b>LPSHDRAGIMAGE</b>

The <a href="https://msdn.microsoft.com/e0dd76b2-fd5c-41e8-b540-db90a2f0dcec">SHDRAGIMAGE</a> structure that contains information about the bitmap.


### -param pDataObject [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the data object's <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because <b>InitializeFromBitmap</b> always performs the RGB multiplication step in calculating the alpha value, you should always pass a bitmap without premultiplied alpha blending. Note that no error will result from passing the method a bitmap with premultiplied alpha blending, but this method will multiply it again, doubling the resulting alpha value.




## -see-also




<a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a>
 

 

