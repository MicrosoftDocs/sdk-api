---
UID: NF:ocidl.IFont.put_Name
title: IFont::put_Name (ocidl.h)
description: Specifies a new name for the font family.
helpviewer_keywords: ["IFont interface [COM]","put_Name method","IFont.put_Name","IFont::put_Name","_ctrl_ifont_put_name","com.ifont_put_name","ocidl/IFont::put_Name","put_Name","put_Name method [COM]","put_Name method [COM]","IFont interface"]
old-location: com\ifont_put_name.htm
tech.root: com
ms.assetid: 3593d5c9-e2b7-4d85-b8f7-94f01a901030
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],put_Name method, IFont.put_Name, IFont::put_Name, _ctrl_ifont_put_name, com.ifont_put_name, ocidl/IFont::put_Name, put_Name, put_Name method [COM], put_Name method [COM],IFont interface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFont::put_Name
 - ocidl/IFont::put_Name
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.put_Name
---

# IFont::put_Name


## -description

Specifies a new name for the font family.

## -parameters

### -param name [in]

The new name of the font family. This value is both allocated and freed by 
      the caller.

## -returns

The method supports the standard return value <b>E_UNEXPECTED</b>, as well as the 
      following values.

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
The name was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>name</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The string value is caller allocated and the caller is responsible for freeing it after this call 
    returns.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_name">IFont::get_Name</a>