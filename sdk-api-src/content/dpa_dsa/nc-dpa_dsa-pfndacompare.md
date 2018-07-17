---
UID: NC:dpa_dsa.PFNDACOMPARE
title: PFNDACOMPARE
author: windows-sdk-content
description: Defines the prototype for the compare function used by DSA_Sort.
old-location: controls\PFNDACOMPARE.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndacompare.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PFNDACOMPARE, PFNDACOMPARE callback, PFNDACOMPARE callback function [Windows Controls], PFNDPACOMPARE, PFNDSACOMPARE, _shell_PFNDACOMPARE, _shell_PFNDACOMPARE_cpp, controls.PFNDACOMPARE, controls._shell_PFNDACOMPARE, dpa_dsa/PFNDACOMPARE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dpa_dsa.h
api_name:
 - PFNDACOMPARE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PFNDACOMPARE callback function


## -description


Defines the prototype for the compare function used by <a href="https://msdn.microsoft.com/cf9c56fd-eeca-414a-8c3f-a962d41b1161">DSA_Sort</a>.


## -parameters




### -param *p1 [in, optional]

Type: <b>void*</b>

A pointer to the first item in the comparison.


### -param *p2 [in, optional]

Type: <b>void*</b>

A pointer to the second item in the comparison.


### -param lParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Additional data passed to <i>pfnCmp</i>.


## -returns



Type: <b>int</b>

The meaning of the return values depends on the function that uses this callback prototype. The return values for <a href="https://msdn.microsoft.com/cf9c56fd-eeca-414a-8c3f-a962d41b1161">DSA_Sort</a> are the following.
                        
                        


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



Alternate names for this callback are <b>PFNDPACOMPARE</b> and <b>PFNDSACOMPARE</b>.



