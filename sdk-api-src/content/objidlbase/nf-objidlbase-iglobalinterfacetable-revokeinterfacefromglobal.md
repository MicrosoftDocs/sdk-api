---
UID: NF:objidlbase.IGlobalInterfaceTable.RevokeInterfaceFromGlobal
title: IGlobalInterfaceTable::RevokeInterfaceFromGlobal (objidlbase.h)
description: Revokes the registration of an interface in the global interface table.
helpviewer_keywords: ["IGlobalInterfaceTable interface [COM]","RevokeInterfaceFromGlobal method","IGlobalInterfaceTable.RevokeInterfaceFromGlobal","IGlobalInterfaceTable::RevokeInterfaceFromGlobal","RevokeInterfaceFromGlobal","RevokeInterfaceFromGlobal method [COM]","RevokeInterfaceFromGlobal method [COM]","IGlobalInterfaceTable interface","_com_iglobalinterfacetable_revokeinterfacefromglobal","com.iglobalinterfacetable_revokeinterfacefromglobal","objidlbase/IGlobalInterfaceTable::RevokeInterfaceFromGlobal"]
old-location: com\iglobalinterfacetable_revokeinterfacefromglobal.htm
tech.root: com
ms.assetid: 202bf33a-5827-4cbf-b977-86167a9c633f
ms.date: 12/05/2018
ms.keywords: IGlobalInterfaceTable interface [COM],RevokeInterfaceFromGlobal method, IGlobalInterfaceTable.RevokeInterfaceFromGlobal, IGlobalInterfaceTable::RevokeInterfaceFromGlobal, RevokeInterfaceFromGlobal, RevokeInterfaceFromGlobal method [COM], RevokeInterfaceFromGlobal method [COM],IGlobalInterfaceTable interface, _com_iglobalinterfacetable_revokeinterfacefromglobal, com.iglobalinterfacetable_revokeinterfacefromglobal, objidlbase/IGlobalInterfaceTable::RevokeInterfaceFromGlobal
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IGlobalInterfaceTable::RevokeInterfaceFromGlobal
 - objidlbase/IGlobalInterfaceTable::RevokeInterfaceFromGlobal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalInterfaceTable.RevokeInterfaceFromGlobal
---

# IGlobalInterfaceTable::RevokeInterfaceFromGlobal


## -description

Revokes the registration of an interface in the global interface table.

## -parameters

### -param dwCookie [in]

Identifies the interface whose global registration is to be revoked.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter is invalid.

</td>
</tr>
</table>

## -remarks

Call this method when an interface registered in the global interface table object no longer needs to be accessed by other apartments in the same process. This method can be called by any apartment in the process, including apartments other than the one that registered the interface in the global interface table.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iglobalinterfacetable">IGlobalInterfaceTable</a>