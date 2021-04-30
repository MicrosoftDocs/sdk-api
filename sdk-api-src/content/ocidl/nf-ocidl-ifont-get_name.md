---
UID: NF:ocidl.IFont.get_Name
title: IFont::get_Name (ocidl.h)
description: Retrieves the name of the font family.
helpviewer_keywords: ["IFont interface [COM]","get_Name method","IFont.get_Name","IFont::get_Name","_ctrl_ifont_get_name","com.ifont_get_name","get_Name","get_Name method [COM]","get_Name method [COM]","IFont interface","ocidl/IFont::get_Name"]
old-location: com\ifont_get_name.htm
tech.root: com
ms.assetid: 04ce50a6-b833-4476-91a9-0d1ca7296314
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],get_Name method, IFont.get_Name, IFont::get_Name, _ctrl_ifont_get_name, com.ifont_get_name, get_Name, get_Name method [COM], get_Name method [COM],IFont interface, ocidl/IFont::get_Name
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
 - IFont::get_Name
 - ocidl/IFont::get_Name
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
 - IFont.get_Name
---

# IFont::get_Name


## -description

Retrieves the name of the font family.

## -parameters

### -param pName [out]

A pointer to the caller-allocated variable that receives the name. This string must be freed with <b>SysFreeString</b> when it is no longer needed.

## -returns

The method supports the standard return value <b>E_UNEXPECTED</b>, as well as the following values.

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
The name was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pname</i> parameter is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_name">IFont::put_Name</a>