---
UID: NF:mfapi.DEFINE_MEDIATYPE_GUID
title: DEFINE_MEDIATYPE_GUID macro
author: windows-sdk-content
description: Defines a media subtype GUID from a FOURCC code, D3DFORMAT value, or audio format type.
old-location: mf\define_mediatype_guid_macro.htm
tech.root: medfound
ms.assetid: be094ccc-a475-480a-a345-bdad70b11f45
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DEFINE_MEDIATYPE_GUID, DEFINE_MEDIATYPE_GUID macro [Media Foundation], be094ccc-a475-480a-a345-bdad70b11f45, mf.define_mediatype_guid_macro, mfapi/DEFINE_MEDIATYPE_GUID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - DEFINE_MEDIATYPE_GUID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

