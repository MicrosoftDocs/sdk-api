---
UID: NC:dpa_dsa.PFNDACOMPARECONST
title: PFNDACOMPARECONST (dpa_dsa.h)
description: Defines the prototype for the compare function used by DSA_Sort when the items being compared are constant objects.
helpviewer_keywords: ["PFNDACOMPARECONST","PFNDACOMPARECONST callback","PFNDACOMPARECONST callback function [Windows Controls]","PFNDPACOMPARECONST","PFNDSACOMPARECONST","_shell_PFNDACOMPARECONST","_shell_PFNDACOMPARECONST_cpp","controls.PFNDACOMPARECONST","controls._shell_PFNDACOMPARECONST","dpa_dsa/PFNDACOMPARECONST"]
old-location: controls\PFNDACOMPARECONST.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndacompareconst.htm
ms.date: 12/05/2018
ms.keywords: PFNDACOMPARECONST, PFNDACOMPARECONST callback, PFNDACOMPARECONST callback function [Windows Controls], PFNDPACOMPARECONST, PFNDSACOMPARECONST, _shell_PFNDACOMPARECONST, _shell_PFNDACOMPARECONST_cpp, controls.PFNDACOMPARECONST, controls._shell_PFNDACOMPARECONST, dpa_dsa/PFNDACOMPARECONST
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNDACOMPARECONST
 - dpa_dsa/PFNDACOMPARECONST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dpa_dsa.h
api_name:
 - PFNDACOMPARECONST
---

# PFNDACOMPARECONST callback function


## -description

Defines the prototype for the compare function used by <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort">DSA_Sort</a> when the items being compared are constant objects.

## -parameters

### -param p1 [in, optional]

Type: <b>const void*</b>

A pointer to the first item in the comparison.

### -param p2 [in, optional]

Type: <b>const void*</b>

A pointer to the second item in the comparison.

### -param lParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Additional data passed to <i>pfnCmp</i>.

## -returns

Type: <b>int</b>

The meaning of the return values depends on the function that uses this callback prototype. The return values for <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort">DSA_Sort</a> are as follows:                
                    


<table class="clsStd">
<tr>
<td>less than 0</td>
<td>If <i>p1</i> should be sorted ahead of <i>p2</i>.</td>
</tr>
<tr>
<td>equal to 0</td>
<td>If <i>p1</i> and <i>p2</i> should be sorted together.</td>
</tr>
<tr>
<td>greater than 0</td>
<td>If <i>p1</i> should be sorted after <i>p2</i>.</td>
</tr>
</table>

## -remarks

Alternate names for this callback are <b>PFNDPACOMPARECONST</b> and <b>PFNDSACOMPARECONST</b>.
