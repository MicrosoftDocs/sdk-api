---
UID: NS:wabdefs._SPropProblemArray
title: SPropProblemArray (wabdefs.h)
description: Do not use. Contains an array of one or more SPropProblem structures.
helpviewer_keywords: ["*LPSPropProblemArray","SPropProblemArray","SPropProblemArray structure [Windows Address Book]","_wab_SPropProblemArray","wab._wab_SPropProblemArray","wabdefs/SPropProblemArray"]
old-location: wab\_wab_SPropProblemArray.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\spropproblemarray.htm
ms.date: 12/05/2018
ms.keywords: '*LPSPropProblemArray, SPropProblemArray, SPropProblemArray structure [Windows Address Book], _wab_SPropProblemArray, wab._wab_SPropProblemArray, wabdefs/SPropProblemArray'
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
req.typenames: SPropProblemArray, *LPSPropProblemArray
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _SPropProblemArray
 - wabdefs/_SPropProblemArray
 - LPSPropProblemArray
 - wabdefs/LPSPropProblemArray
 - SPropProblemArray
 - wabdefs/SPropProblemArray
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
 - SPropProblemArray
---

# SPropProblemArray structure


## -description

Do not use. Contains an array of one or more <a href="/windows/desktop/api/wabdefs/ns-wabdefs-spropproblem">SPropProblem</a> structures.

## -struct-fields

### -field cProblem

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the count of <a href="/windows/desktop/api/wabdefs/ns-wabdefs-spropproblem">SPropProblem</a> structures in the array indicated by the <b>aProblem</b> member.

### -field aProblem

Type: <b><a href="/windows/desktop/api/wabdefs/ns-wabdefs-spropproblem">SPropProblem</a>[MAPI_DIM]</b>

Array of variables of type <a href="/windows/desktop/api/wabdefs/ns-wabdefs-spropproblem">SPropProblem</a> that specify information about a property error.