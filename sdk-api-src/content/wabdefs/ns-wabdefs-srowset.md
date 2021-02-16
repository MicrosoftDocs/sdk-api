---
UID: NS:wabdefs._SRowSet
title: SRowSet (wabdefs.h)
description: Do not use. Contains an array of SRow structures. Each SRow structure describes a row from a table.
helpviewer_keywords: ["*LPSRowSet","SRowSet","SRowSet structure [Windows Address Book]","_wab_SRowSet","wab._wab_SRowSet","wabdefs/SRowSet"]
old-location: wab\_wab_SRowSet.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\srowset.htm
ms.date: 12/05/2018
ms.keywords: '*LPSRowSet, SRowSet, SRowSet structure [Windows Address Book], _wab_SRowSet, wab._wab_SRowSet, wabdefs/SRowSet'
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SRowSet, *LPSRowSet
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _SRowSet
 - wabdefs/_SRowSet
 - LPSRowSet
 - wabdefs/LPSRowSet
 - SRowSet
 - wabdefs/SRowSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SRowSet
---

# SRowSet structure


## -description

Do not use. Contains an array of <a href="/windows/desktop/api/wabdefs/ns-wabdefs-srow">SRow</a> structures. Each <b>SRow</b> structure describes a row from a table.

## -struct-fields

### -field cRows

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of <a href="/windows/desktop/api/wabdefs/ns-wabdefs-srow">SRow</a> structures in the <b>aRow</b> member.

### -field aRow

Type: <b><a href="/windows/desktop/api/wabdefs/ns-wabdefs-srow">SRow</a>[MAPI_DIM]</b>

Array of variables of type <a href="/windows/desktop/api/wabdefs/ns-wabdefs-srow">SRow</a> that specifies the structures that represent the rows in the table.