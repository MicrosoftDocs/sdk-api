---
UID: NF:dsattrib.IAttributeGet.GetCount
title: IAttributeGet::GetCount (dsattrib.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCount","GetCount method [Microsoft TV Technologies]","GetCount method [Microsoft TV Technologies]","IAttributeGet interface","IAttributeGet interface [Microsoft TV Technologies]","GetCount method","IAttributeGet.GetCount","IAttributeGet::GetCount","IAttributeGetGetCount","dsattrib/IAttributeGet::GetCount","mstv.iattributeget_getcount"]
old-location: mstv\iattributeget_getcount.htm
tech.root: mstv
ms.assetid: 340a0a0d-26e9-4c63-8552-15f7c841c759
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Microsoft TV Technologies], GetCount method [Microsoft TV Technologies],IAttributeGet interface, IAttributeGet interface [Microsoft TV Technologies],GetCount method, IAttributeGet.GetCount, IAttributeGet::GetCount, IAttributeGetGetCount, dsattrib/IAttributeGet::GetCount, mstv.iattributeget_getcount
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
 - IAttributeGet::GetCount
 - dsattrib/IAttributeGet::GetCount
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
 - IAttributeGet.GetCount
---

# IAttributeGet::GetCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCount</b> method returns the number of attributes on this object.

## -parameters

### -param plCount [out]

Receives the number of attributes.

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