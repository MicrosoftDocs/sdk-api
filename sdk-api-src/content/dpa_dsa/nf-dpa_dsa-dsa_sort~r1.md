---
UID: NF:dpa_dsa.DSA_Sort~r1
title: DSA_Sort
ms.date: 01/30/19
ms.keywords: DSA_Sort
f1_keywords:
- dpa_dsa/DSA_Sort
dev_langs:
- c++
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dpa_dsa.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- 
api_location:
- dpa_dsa.h
api_name:
- DSA_Sort
---

# DSA_Sort function


## -description

Sorts the items in a dynamic structure array (DSA).


## -parameters

### -param hdsa

Type: <b>HDSA</b>

A handle to an existing DSA.


### -param pfnCompare

Type: <b>PFNDACOMPARECONST</b>

A comparison function pointer. 


### -param lParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.


## -returns

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> on success or <b>FALSE</b> on failure.

## -remarks

## -see-also

