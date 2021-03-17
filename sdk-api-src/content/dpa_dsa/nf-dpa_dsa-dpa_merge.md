---
UID: NF:dpa_dsa.DPA_Merge
title: DPA_Merge function (dpa_dsa.h)
description: Combines the contents of two dynamic pointer arrays (DPAs).
helpviewer_keywords: ["DPAM_INTERSECT","DPAM_NORMAL","DPAM_SORTED","DPAM_UNION","DPA_Merge","DPA_Merge function [Windows Controls]","_shell_DPA_Merge","_shell_DPA_Merge_cpp","controls.DPA_Merge","controls._shell_DPA_Merge","dpa_dsa/DPA_Merge"]
old-location: controls\DPA_Merge.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_merge.htm
ms.date: 12/05/2018
ms.keywords: DPAM_INTERSECT, DPAM_NORMAL, DPAM_SORTED, DPAM_UNION, DPA_Merge, DPA_Merge function [Windows Controls], _shell_DPA_Merge, _shell_DPA_Merge_cpp, controls.DPA_Merge, controls._shell_DPA_Merge, dpa_dsa/DPA_Merge
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Comctl32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DPA_Merge
 - dpa_dsa/DPA_Merge
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
 - DPA_Merge
---

# DPA_Merge function


## -description

<p class="CCE_Message">[<b>DPA_Merge</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Combines the contents of two dynamic pointer arrays (DPAs).

## -parameters

### -param hdpaDest [in, out]

Type: <b>HDPA</b>

A handle to the first DPA. This array can be optionally presorted. When this function returns, contains the handle to the merged array.

### -param hdpaSrc [in]

Type: <b>HDPA</b>

A handle to the second DPA. This array can be optionally presorted.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Options determining the method used to merge the two arrays. DPAM_NORMAL, DPAM_UNION, and DPAM_UNION are mutually exclusive—only one of those flags can be set, optionally in conjunction with DPAM_SORTED.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DPAM_SORTED"></a><a id="dpam_sorted"></a><dl>
<dt><b>DPAM_SORTED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The arrays are presorted; skip sorting. If this flag is not set, the arrays are sorted before they are merged.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAM_NORMAL"></a><a id="dpam_normal"></a><dl>
<dt><b>DPAM_NORMAL</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The final array consists of all of the elements originally present in <i>hdpaDest</i>. If any of those elements are also found in <i>hdpaSrc</i>, those elements are merged in the final array. The <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge">PFNDPAMERGE</a> callback function is called with the DPAMM_MERGE message.

                        

When this flag is set, the final size of the array at <i>hdpaDest</i> is the same as its initial size.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAM_UNION"></a><a id="dpam_union"></a><dl>
<dt><b>DPAM_UNION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The final array is the union of all elements in both arrays. Elements found in both arrays are merged in the final array. Elements found in only one array or the other are added as found. When this flag is set, the <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge">PFNDPAMERGE</a> callback function can be called with the DPAMM_MERGE or DPAMM_INSERT message. 

                        

The final size of the array is at least the size of the larger of <i>hdpaDest</i> and <i>hdpaSrc</i>, and at most the sum of the two.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAM_INTERSECT"></a><a id="dpam_intersect"></a><dl>
<dt><b>DPAM_INTERSECT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Only elements found in both <i>hdpaSrc</i> and <i>hdpaDest</i> are merged to form the final array. When this flag is set, the <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge">PFNDPAMERGE</a> callback function can be called with the DPAMM_MERGE or DPAMM_DELETE message. 

                        

The final size of the array can range between 0 and the smaller of <i>hdpaDest</i> and <i>hdpaSrc</i>.

</td>
</tr>
</table>

### -param pfnCompare [in]

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a></b>

The <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a> callback function that compares two elements, one from each DPA, to determine whether they are the same item. If so, the callback function pointed to by <i>pfnCompare</i> is called.

### -param pfnMerge [in]

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge">PFNDPAMERGE</a></b>

The <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge">PFNDPAMERGE</a> callback function that merges the contents when an element is found in both DPAs and is found to be the same item by <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a>.

### -param lParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Additional parameter used to declare the basis of comparison upon which equality is determined.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

<b>DPA_Merge</b> is not exported by name. To use it, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 11 from ComCtl32.dll to obtain a function pointer.