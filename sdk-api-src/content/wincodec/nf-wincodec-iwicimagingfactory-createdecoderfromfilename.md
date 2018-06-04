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

# IWICImagingFactory::CreateDecoderFromFilename


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> class based on the given file.


## -parameters




### -param wzFilename [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated string that specifies the name of an object to create or open.


### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred decoder vendor. Use <b>NULL</b> if no preferred vendor.


### -param dwDesiredAccess [in]

Type: <b>DWORD</b>


               The access to the object, which can be read, write, or both.
               

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>GENERIC_READ</dt>
</dl>
</td>
<td width="60%">
Read access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>GENERIC_WRITE</dt>
</dl>
</td>
<td width="60%">
Write access.

</td>
</tr>
</table>
 

For more information, see <a href="https://msdn.microsoft.com/e18cede9-9bf7-4866-850b-5d7fa43a5b0f">Generic Access Rights</a>.


### -param metadataOptions [in]

Type: <b><a href="https://msdn.microsoft.com/27b9d6e1-e171-4c7f-8f96-fa5a93923e35">WICDecodeOptions</a></b>

The <a href="https://msdn.microsoft.com/27b9d6e1-e171-4c7f-8f96-fa5a93923e35">WICDecodeOptions</a> to use when creating the decoder.


### -param ppIDecoder [out, retval]

Type: <b><a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>**</b>

A pointer that receives a pointer to the new <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



