---
UID: NF:dpa_dsa.DSA_Sort
title: DSA_Sort function (dpa_dsa.h)
description: Sorts the items in a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_Sort","DSA_Sort function [Windows Controls]","_shell_DSA_Sort","_shell_DSA_Sort_cpp","controls.DSA_Sort","controls._shell_DSA_Sort","dpa_dsa/DSA_Sort"]
old-location: controls\DSA_Sort.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_sort.htm
ms.date: 12/05/2018
ms.keywords: DSA_Sort, DSA_Sort function [Windows Controls], _shell_DSA_Sort, _shell_DSA_Sort_cpp, controls.DSA_Sort, controls._shell_DSA_Sort, dpa_dsa/DSA_Sort
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DSA_Sort
 - dpa_dsa/DSA_Sort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_Sort
---

# DSA_Sort function


## -description

Sorts the items in a dynamic structure array (DSA).

## -parameters

### -param pdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.

### -param pfnCompare [in]

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDACOMPARE</a></b>

A comparison function pointer. See <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a> for the comparison function prototype.

### -param lParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> on success or <b>FALSE</b> on failure.