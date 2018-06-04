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

# ISoftwareBitmapNativeFactory::imaging


## -description


Creates an <a href="https://msdn.microsoft.com/9EB9C74E-A056-4A40-AFAD-0056E139BA28">ISoftwareBitmapNative</a>  from the provided <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>.


## -parameters




### -param data [in]

Type: <b>IWICBitmap*</b>

The source WIC bitmap.


### -param forceReadOnly [in]

Type: <b>BOOL</b>

A value indicating whether the created software bitmap is read-only.

<div class="alert"><b>Note</b>  The read-only access applies only to the Windows Runtime<a href="https://msdn.microsoft.com/cf4130af-344e-454e-ab61-a8238db94a06">SoftwareBitmap</a> wrapper. Access to the underlying Media Foundation buffer is not restricted.</div>
<div> </div>

### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://msdn.microsoft.com/9EB9C74E-A056-4A40-AFAD-0056E139BA28">ISoftwareBitmapNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://msdn.microsoft.com/613BFE81-AC55-4786-B6BD-0FFB7506D7F1">ISoftwareBitmapNativeFactory</a>
 

 

