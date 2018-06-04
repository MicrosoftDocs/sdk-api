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

# IAssemblyCacheItem::CreateStream


## -description


The <b>CreateStream</b> method copies the source of a manifest or module into a stream.


## -parameters




### -param dwFlags [in]

Reserved.


### -param pszStreamName [in]

Pointer to a string value containing the name of the manifest. This becomes the name of the stream.


### -param dwFormat [in]

This parameter specifies whether a module or manifest is being copied to a stream.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STREAM_FORMAT_COMPLIB_MODULE"></a><a id="stream_format_complib_module"></a><dl>
<dt><b>STREAM_FORMAT_COMPLIB_MODULE</b></dt>
</dl>
</td>
<td width="60%">
Copy  the source  of a module for a non-Windows assembly to a stream.

</td>
</tr>
<tr>
<td width="40%"><a id="STREAM_FORMAT_COMPLIB_MANIFEST"></a><a id="stream_format_complib_manifest"></a><dl>
<dt><b>STREAM_FORMAT_COMPLIB_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
Copy  the source  of a manifest for a non-Windows assembly to a stream.

</td>
</tr>
<tr>
<td width="40%"><a id="STREAM_FORMAT_WIN32_MODULE"></a><a id="stream_format_win32_module"></a><dl>
<dt><b>STREAM_FORMAT_WIN32_MODULE</b></dt>
</dl>
</td>
<td width="60%">
Copy  the source  of a module for a Windows assembly to a stream.

</td>
</tr>
<tr>
<td width="40%"><a id="STREAM_FORMAT_WIN32_MANIFEST"></a><a id="stream_format_win32_manifest"></a><dl>
<dt><b>STREAM_FORMAT_WIN32_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
Copy  the source  of a manifest for a Windows assembly to a stream.

</td>
</tr>
</table>
 


### -param dwFormatFlags [in]

Reserved.


### -param ppIStream

Pointer to the location that contains the pointer to the IStream interface that receives the information.


### -param puliMaxSize [optional]

Reserved.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The method did not succeed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9df9ee58-0354-49f0-af9c-5b92179cfaea">IAssemblyCacheItem</a>
 

 

