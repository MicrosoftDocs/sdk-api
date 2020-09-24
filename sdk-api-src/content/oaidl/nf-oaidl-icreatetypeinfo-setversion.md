---
UID: NF:oaidl.ICreateTypeInfo.SetVersion
title: ICreateTypeInfo::SetVersion (oaidl.h)
description: Sets the major and minor version number of the type information.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetVersion method","ICreateTypeInfo.SetVersion","ICreateTypeInfo::SetVersion","SetVersion","SetVersion method [Automation]","SetVersion method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetVersion","automat.icreatetypeinfo_setversion","oaidl/ICreateTypeInfo::SetVersion"]
old-location: automat\icreatetypeinfo_setversion.htm
tech.root: automat
ms.assetid: ffa4d287-44c4-40ec-984a-70cbc0928274
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetVersion method, ICreateTypeInfo.SetVersion, ICreateTypeInfo::SetVersion, SetVersion, SetVersion method [Automation], SetVersion method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetVersion, automat.icreatetypeinfo_setversion, oaidl/ICreateTypeInfo::SetVersion
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - ICreateTypeInfo::SetVersion
 - oaidl/ICreateTypeInfo::SetVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeInfo.SetVersion
---

# ICreateTypeInfo::SetVersion


## -description

Sets the major and minor version number of the type information.

## -parameters

### -param wMajorVerNum [in]

The major version number.

### -param wMinorVerNum [in]

The minor version number.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot write to the destination.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.


</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>