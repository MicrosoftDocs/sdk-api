---
UID: NF:ocidl.IFont.get_hFont
title: IFont::get_hFont
author: windows-sdk-content
description: Retrieves a handle to the font described by this font object.
old-location: com\ifont_get_hfont.htm
tech.root: com
ms.assetid: 19bfd78a-0e81-45c3-a3b8-bc893669e9f5
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IFont interface [COM],get_hFont method, IFont.get_hFont, IFont::get_hFont, _ctrl_ifont_get_hfont, com.ifont_get_hfont, get_hFont, get_hFont method [COM], get_hFont method [COM],IFont interface, ocidl/IFont::get_hFont
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.get_hFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::get_hFont


## -description


Retrieves a handle to the font described by this font object.


## -parameters




### -param phFont [out]

A pointer to the caller-allocated variable that receives the font handle. 
      The caller does not own this resource and must not attempt to destroy the font.


## -returns



The method supports the standard return values <b>E_UNEXPECTED</b> and 
      <b>E_OUTOFMEMORY</b>, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The font handle was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>phFont</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The font object maintains ownership of the <b>HFONT</b> and can destroy it 
    at any time without prior notification. If the caller needs to secure this font for a limited period of time, it 
    can call <a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a> and 
    <a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">IFont::ReleaseHfont</a>.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a>



<a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">IFont::ReleaseHfont</a>
 

 

