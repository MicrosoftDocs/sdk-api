---
UID: NF:ocidl.IFont.Clone
title: IFont::Clone (ocidl.h)
description: Creates a duplicate font object.
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IFont interface","IFont interface [COM]","Clone method","IFont.Clone","IFont::Clone","_ctrl_ifont_clone","com.ifont_clone","ocidl/IFont::Clone"]
old-location: com\ifont_clone.htm
tech.root: com
ms.assetid: de5da0d1-338a-455c-a04b-99dc025b95bb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IFont interface, IFont interface [COM],Clone method, IFont.Clone, IFont::Clone, _ctrl_ifont_clone, com.ifont_clone, ocidl/IFont::Clone
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
 - IFont::Clone
 - ocidl/IFont::Clone
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
 - IFont.Clone
---

# IFont::Clone


## -description

Creates a duplicate font object with a state identical to the current font.

## -parameters

### -param ppFont [out]

Address of <a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a> pointer variable that receives the interface 
       pointer to the new font object. The caller must call 
       <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IFont::Release</a> when this new font object is no longer 
       needed.

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
The new font object was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This font object does not support cloning.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppfont</i> is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The new font object is entirely independent of the first. The caller is responsible for releasing this new 
     object when it is no longer needed. This method does not affect the reference count of the font being cloned.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>