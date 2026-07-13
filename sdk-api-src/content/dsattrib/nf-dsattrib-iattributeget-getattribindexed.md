---
UID: NF:dsattrib.IAttributeGet.GetAttribIndexed
title: IAttributeGet::GetAttribIndexed (dsattrib.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetAttribIndexed","GetAttribIndexed method [Microsoft TV Technologies]","GetAttribIndexed method [Microsoft TV Technologies]","IAttributeGet interface","IAttributeGet interface [Microsoft TV Technologies]","GetAttribIndexed method","IAttributeGet.GetAttribIndexed","IAttributeGet::GetAttribIndexed","IAttributeGetGetAttribIndexed","dsattrib/IAttributeGet::GetAttribIndexed","mstv.iattributeget_getattribindexed"]
old-location: mstv\iattributeget_getattribindexed.htm
tech.root: mstv
ms.assetid: 30fdd27f-99df-4ed6-b9ce-514b0e358854
ms.date: 12/05/2018
ms.keywords: GetAttribIndexed, GetAttribIndexed method [Microsoft TV Technologies], GetAttribIndexed method [Microsoft TV Technologies],IAttributeGet interface, IAttributeGet interface [Microsoft TV Technologies],GetAttribIndexed method, IAttributeGet.GetAttribIndexed, IAttributeGet::GetAttribIndexed, IAttributeGetGetAttribIndexed, dsattrib/IAttributeGet::GetAttribIndexed, mstv.iattributeget_getattribindexed
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
 - IAttributeGet::GetAttribIndexed
 - dsattrib/IAttributeGet::GetAttribIndexed
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
 - IAttributeGet.GetAttribIndexed
---

# IAttributeGet::GetAttribIndexed


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetAttribIndexed</b> method returns an attribute value, specified by index.

## -parameters

### -param lIndex [in]

Zero-based index of the attribute. To get the number of attributes, call <a href="/previous-versions/windows/desktop/api/dsattrib/nf-dsattrib-iattributeget-getcount">IAttributeGet::GetCount</a>.

### -param pguidAttribute [out]

Receives the <b>GUID</b> for this attribute.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lIndex</i> parameter is out of range.

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