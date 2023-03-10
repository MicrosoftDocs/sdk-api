---
UID: NF:oaidl.ICreateTypeLib.SetVersion
title: ICreateTypeLib::SetVersion (oaidl.h)
description: Sets the major and minor version numbers of the type library.
helpviewer_keywords: ["ICreateTypeLib interface [Automation]","SetVersion method","ICreateTypeLib.SetVersion","ICreateTypeLib::SetVersion","SetVersion","SetVersion method [Automation]","SetVersion method [Automation]","ICreateTypeLib interface","_oa96_ICreateTypeLib_SetVersion","automat.icreatetypelib_setversion","oaidl/ICreateTypeLib::SetVersion"]
old-location: automat\icreatetypelib_setversion.htm
tech.root: automat
ms.assetid: 1c71bf8f-998a-4a9a-a4a8-981f51334cbe
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib interface [Automation],SetVersion method, ICreateTypeLib.SetVersion, ICreateTypeLib::SetVersion, SetVersion, SetVersion method [Automation], SetVersion method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetVersion, automat.icreatetypelib_setversion, oaidl/ICreateTypeLib::SetVersion
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
 - ICreateTypeLib::SetVersion
 - oaidl/ICreateTypeLib::SetVersion
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
 - ICreateTypeLib.SetVersion
---

# ICreateTypeLib::SetVersion


## -description

Sets the major and minor version numbers of the type library.

## -parameters

### -param wMajorVerNum [in]

The major version number for the library.

### -param wMinorVerNum [in]

The minor version number for the library.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>