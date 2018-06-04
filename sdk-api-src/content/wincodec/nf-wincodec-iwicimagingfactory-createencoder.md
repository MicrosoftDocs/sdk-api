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

# IWICImagingFactory::CreateEncoder


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a> class.


## -parameters




### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The GUID for the desired container format.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatBmp</dt>
</dl>
</td>
<td width="60%">
The BMP container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatPng</dt>
</dl>
</td>
<td width="60%">
The PNG container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatIco</dt>
</dl>
</td>
<td width="60%">
The ICO container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatJpeg</dt>
</dl>
</td>
<td width="60%">
The JPEG container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatTiff</dt>
</dl>
</td>
<td width="60%">
The TIFF container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatGif</dt>
</dl>
</td>
<td width="60%">
The GIF container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatWmp</dt>
</dl>
</td>
<td width="60%">
The HD Photo container format GUID.

</td>
</tr>
</table>
 


### -param pguidVendor [in, optional]

Type: <b>const GUID*</b>

The GUID for the preferred encoder vendor. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>NULL</dt>
</dl>
</td>
<td width="60%">
No preferred codec vendor.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_VendorMicrosoft</dt>
</dl>
</td>
<td width="60%">
Prefer to use Microsoft encoder.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_VendorMicrosoftBuiltIn</dt>
</dl>
</td>
<td width="60%">
Prefer to use the native Microsoft encoder.

</td>
</tr>
</table>
 


### -param ppIEncoder [out, retval]

Type: <b><a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            Other values may be available for both <i>guidContainerFormat</i> and <i>pguidVendor</i> depending on the installed WIC-enabled encoders.
            The values listed are those that are natively supported by the operating system.
         




## -see-also




<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>
 

 

