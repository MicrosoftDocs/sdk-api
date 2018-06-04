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

# IWiaVideo::TakePicture


## -description


The <b>IWiaVideo::TakePicture</b> method extracts a still image from the video stream, and saves the image as a JPEG file.


## -parameters




### -param pbstrNewImageFilename [out]

Type: <b>BSTR*</b>

Receives the full path and filename of the JPEG file that this method creates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The path and directory where the image file is saved are specified by the <a href="https://msdn.microsoft.com/f7bff8d2-1cdd-4d32-877b-c61343888a26">IWiaVideo::ImagesDirectory</a> property.



