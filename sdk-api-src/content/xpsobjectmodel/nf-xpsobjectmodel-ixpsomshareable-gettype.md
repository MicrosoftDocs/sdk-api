---
UID: NF:xpsobjectmodel.IXpsOMShareable.GetType
title: IXpsOMShareable::GetType (xpsobjectmodel.h)
description: Gets the object type of the interface.
helpviewer_keywords: ["GetType","GetType method [XPS Documents and Packaging]","GetType method [XPS Documents and Packaging]","IXpsOMShareable interface","IXpsOMShareable interface [XPS Documents and Packaging]","GetType method","IXpsOMShareable.GetType","IXpsOMShareable::GetType","xps.ixpsomshareable_gettype","xpsobjectmodel/IXpsOMShareable::GetType"]
old-location: xps\ixpsomshareable_gettype.htm
tech.root: xps
ms.assetid: 1d30e11e-1306-4721-b5fc-0419715ba2c8
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [XPS Documents and Packaging], GetType method [XPS Documents and Packaging],IXpsOMShareable interface, IXpsOMShareable interface [XPS Documents and Packaging],GetType method, IXpsOMShareable.GetType, IXpsOMShareable::GetType, xps.ixpsomshareable_gettype, xpsobjectmodel/IXpsOMShareable::GetType
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - IXpsOMShareable::GetType
 - xpsobjectmodel/IXpsOMShareable::GetType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMShareable.GetType
---

# IXpsOMShareable::GetType


## -description

Gets the object type of the interface.

## -parameters

### -param type [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_object_type">XPS_OBJECT_TYPE</a> value that describes the interface that is derived from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>type</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>