---
UID: NF:dsattrib.IAttributeGet.GetAttrib
title: IAttributeGet::GetAttrib (dsattrib.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetAttrib","GetAttrib method [Microsoft TV Technologies]","GetAttrib method [Microsoft TV Technologies]","IAttributeGet interface","IAttributeGet interface [Microsoft TV Technologies]","GetAttrib method","IAttributeGet.GetAttrib","IAttributeGet::GetAttrib","IAttributeGetGetAttrib","dsattrib/IAttributeGet::GetAttrib","mstv.iattributeget_getattrib"]
old-location: mstv\iattributeget_getattrib.htm
tech.root: mstv
ms.assetid: df1aad0c-7e71-4110-8e05-0af33dd04859
ms.date: 12/05/2018
ms.keywords: GetAttrib, GetAttrib method [Microsoft TV Technologies], GetAttrib method [Microsoft TV Technologies],IAttributeGet interface, IAttributeGet interface [Microsoft TV Technologies],GetAttrib method, IAttributeGet.GetAttrib, IAttributeGet::GetAttrib, IAttributeGetGetAttrib, dsattrib/IAttributeGet::GetAttrib, mstv.iattributeget_getattrib
req.header: dsattrib.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAttributeGet::GetAttrib
 - dsattrib/IAttributeGet::GetAttrib
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dsattrib.h
api_name:
 - IAttributeGet.GetAttrib
---

# IAttributeGet::GetAttrib


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetAttrib</b> method returns an attribute value, specified by <b>GUID</b>.

## -parameters

### -param guidAttribute [in]

<b>GUID</b> that specifies the attribute to retrieve.

### -param pbAttribute [in, out]

Pointer to a buffer that receives the attribute value. This parameter can be <b>NULL</b>.

### -param pdwAttributeLength [in, out]

If <i>pbAttribute</i> is <b>NULL</b>, this parameter receives the size of the attribute data, in bytes. If <i>pbAttribute</i> is non-<b>NULL</b>, this parameter specifies the size of the <i>pbAttribute</i> buffer, in bytes.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The specified <b>GUID</b> does not match any attribute on this object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dsattrib/nn-dsattrib-iattributeget">IAttributeGet Interface</a>