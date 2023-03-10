---
UID: NF:oaidl.ICreateTypeLib.SaveAllChanges
title: ICreateTypeLib::SaveAllChanges (oaidl.h)
description: Saves the ICreateTypeLib instance following the layout of type information.
helpviewer_keywords: ["ICreateTypeLib interface [Automation]","SaveAllChanges method","ICreateTypeLib.SaveAllChanges","ICreateTypeLib::SaveAllChanges","SaveAllChanges","SaveAllChanges method [Automation]","SaveAllChanges method [Automation]","ICreateTypeLib interface","_oa96_ICreateTypeLib_SaveAllChanges","automat.icreatetypelib_saveallchanges","oaidl/ICreateTypeLib::SaveAllChanges"]
old-location: automat\icreatetypelib_saveallchanges.htm
tech.root: automat
ms.assetid: 67824f38-e515-487e-8f4b-6682a5ac669c
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib interface [Automation],SaveAllChanges method, ICreateTypeLib.SaveAllChanges, ICreateTypeLib::SaveAllChanges, SaveAllChanges, SaveAllChanges method [Automation], SaveAllChanges method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SaveAllChanges, automat.icreatetypelib_saveallchanges, oaidl/ICreateTypeLib::SaveAllChanges
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
 - ICreateTypeLib::SaveAllChanges
 - oaidl/ICreateTypeLib::SaveAllChanges
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
 - ICreateTypeLib.SaveAllChanges
---

# ICreateTypeLib::SaveAllChanges


## -description

Saves the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a> instance following the layout of type information.



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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_IOERROR</b></dt>
</dl>
</td>
<td width="60%">
The function cannot write to the file.

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

## -remarks

You should not call any other <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a> methods after calling <b>SaveAllChanges</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>
