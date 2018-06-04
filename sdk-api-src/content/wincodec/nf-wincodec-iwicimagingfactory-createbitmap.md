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

# IWICImagingFactory::CreateBitmap


## -description


Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> object.


## -parameters




### -param uiWidth [in]

Type: <b>UINT</b>

The width of the new bitmap .


### -param uiHeight [in]

Type: <b>UINT</b>

The height of the new bitmap.


### -param pixelFormat [in]

Type: <b>REFWICPixelFormatGUID</b>

The pixel format of the new bitmap.


### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/121d394d-e818-44c5-bf44-3b01df61c780">WICBitmapCreateCacheOption</a></b>

The cache creation options of the new bitmap. This can be one of the values in the <a href="https://msdn.microsoft.com/121d394d-e818-44c5-bf44-3b01df61c780">WICBitmapCreateCacheOption</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnDemand"></a><a id="wicbitmapcacheondemand"></a><a id="WICBITMAPCACHEONDEMAND"></a><dl>
<dt><b>WICBitmapCacheOnDemand</b></dt>
</dl>
</td>
<td width="60%">
Allocates system memory for the bitmap at initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnLoad"></a><a id="wicbitmapcacheonload"></a><a id="WICBITMAPCACHEONLOAD"></a><dl>
<dt><b>WICBitmapCacheOnLoad</b></dt>
</dl>
</td>
<td width="60%">
Allocates system memory for the bitmap when the bitmap is first used.

</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapNoCache"></a><a id="wicbitmapnocache"></a><a id="WICBITMAPNOCACHE"></a><dl>
<dt><b>WICBitmapNoCache</b></dt>
</dl>
</td>
<td width="60%">
This option is not valid for this method and should not be used.

</td>
</tr>
</table>
 


### -param ppIBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/348b6d15-e339-4dce-99f3-4d639ee9bf7d">Native Pixel Formats</a>
 

 

