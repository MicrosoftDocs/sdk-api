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

# DEFINE_MEDIATYPE_GUID macro


## -description


Defines a media subtype GUID from a FOURCC code, <b>D3DFORMAT</b> value, or audio format type.


## -parameters




### -param name

The name of the GUID constant to be defined.


### -param format

A FOURCC code, D3DFORMAT value, or audio format type.


## -remarks



Media formats are often identified by a FOURCC code (such as 'AYUV'), <b>D3DFORMAT</b> value (such as D3DFMT_X8R8G8B8), or audio format type (such as WAVE_FORMAT_PCM). The <b>DEFINE_MEDIATYPE_GUID</b> macro defines a new GUID constant from one of these values. The resulting GUID can be used as a media subtype.

This macro invokes the <b>DEFINE_GUID</b> macro. The resuling GUID constant is declared <code>extern</code>, so the declaration must have global scope.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;initguid.h&gt;

// Declares a GUID named MFVideoFormat_ABCD_Format.
DEFINE_MEDIATYPE_GUID( MFVideoFormat_ABCD_Format, FCC('ABCD') );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8e600943-92f1-4936-8c00-842fc7f4cb57">MF_MT_SUBTYPE</a>



<a href="https://msdn.microsoft.com/c460b1cd-13d7-4b65-a755-23b2ea87864d">Media Foundation Macros</a>



<a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Media Type GUIDs</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

