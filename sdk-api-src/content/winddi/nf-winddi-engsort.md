---
UID: NF:winddi.EngSort
title: EngSort function (winddi.h)
description: The EngSort function performs a quick-sort on the specified list.
helpviewer_keywords: ["EngSort","EngSort function [Display Devices]","display.engsort","gdifncs_d675bef7-30d0-4e0d-a798-a397b282ce48.xml","winddi/EngSort"]
old-location: display\engsort.htm
tech.root: display
ms.assetid: e3d1864e-97da-4085-89fa-86135a687f60
ms.date: 12/05/2018
ms.keywords: EngSort, EngSort function [Display Devices], display.engsort, gdifncs_d675bef7-30d0-4e0d-a798-a397b282ce48.xml, winddi/EngSort
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngSort
 - winddi/EngSort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngSort
---

# EngSort function


## -description

The <b>EngSort</b> function performs a quick-sort on the specified list.

## -parameters

### -param pjBuf [in, out]

Pointer to the data array to be sorted.

### -param c [in]

Specifies the size, in bytes, of each element in <i>pjBuf</i>.

### -param cjElem [in]

Specifies the number of elements in <i>pjBuf</i> to be sorted.

### -param pfnComp [in]

Pointer to a function that implements the element comparison to be used for the sort.

## -returns

None

## -remarks

<b>EngSort</b> implements a quick-sort algorithm to sort <i>cjElem</i> elements in <i>pjBuf</i>, where each element is of size <i>c</i>. The sorted elements are returned in <i>pjBuf</i>; that is, the original contents of the buffer are overwritten with the sorted results.

The basis for comparing two elements is defined in the function that <i>pfnComp </i> points to. This function is prototyped as follows:


```
int (__cdecl *SORTCOMP)(const void *pv1, const void *pv2);
```


where <i>pv1</i> and <i>pv2</i> point to the two elements to be compared. The return value is the result of the comparison defined as follows:

<table>
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
Negative integer

</td>
<td>
<i>*pv1</i> &lt; <i>*pv2</i>

</td>
</tr>
<tr>
<td>
Zero

</td>
<td>
<i>*pv1</i> == <i>*pv2</i>

</td>
</tr>
<tr>
<td>
Positive integer

</td>
<td>
<i>*pv1</i> &gt; <i>*pv2</i>

</td>
</tr>
</table>
 

The array is sorted in increasing order, which is defined by the <i>pfnComp</i> parameter.

