---
UID: NC:dpa_dsa.PFNDPAMERGECONST
title: PFNDPAMERGECONST (dpa_dsa.h)
description: Defines the prototype for the merge function used by DPA_Merge, using constant values.
helpviewer_keywords: ["DPAMM_DELETE","DPAMM_INSERT","DPAMM_MERGE","PFNDPAMERGECONST","PFNDPAMERGECONST callback","PFNDPAMERGECONST callback function [Windows Controls]","_shell_PFNDPAMERGECONST","_shell_PFNDPAMERGECONST_cpp","controls.PFNDPAMERGECONST","controls._shell_PFNDPAMERGECONST","dpa_dsa/PFNDPAMERGECONST"]
old-location: controls\PFNDPAMERGECONST.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndpamergeconst.htm
ms.date: 12/05/2018
ms.keywords: DPAMM_DELETE, DPAMM_INSERT, DPAMM_MERGE, PFNDPAMERGECONST, PFNDPAMERGECONST callback, PFNDPAMERGECONST callback function [Windows Controls], _shell_PFNDPAMERGECONST, _shell_PFNDPAMERGECONST_cpp, controls.PFNDPAMERGECONST, controls._shell_PFNDPAMERGECONST, dpa_dsa/PFNDPAMERGECONST
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNDPAMERGECONST
 - dpa_dsa/PFNDPAMERGECONST
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
 - PFNDPAMERGECONST
---

# PFNDPAMERGECONST callback function


## -description

Defines the prototype for the merge function used by <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_merge">DPA_Merge</a>, using constant values.

## -parameters

### -param uMsg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A message that instructs this function how to handle the merge. One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DPAMM_MERGE"></a><a id="dpamm_merge"></a><dl>
<dt><b>DPAMM_MERGE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Perform any additional processing needed when merging <i>p2</i> into <i>p1</i>. The function should return a pointer to an item that contains the result of the merge.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAMM_DELETE"></a><a id="dpamm_delete"></a><dl>
<dt><b>DPAMM_DELETE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Perform any additional processing needed when a delete occurs as part of the merge. The function should return <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAMM_INSERT"></a><a id="dpamm_insert"></a><dl>
<dt><b>DPAMM_INSERT</b></dt>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
Perform any user-defined processing when the merge results in an item being inserted as part of the merge. The return value of this function should point to the item result that is inserted as part of the merge.

</td>
</tr>
</table>

### -param pvDest [in]

Type: <b>const void*</b>

A pointer to the destination item in the merge.

### -param pvSrc [in]

Type: <b>const void*</b>

A pointer to the source item in the merge.

### -param lParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Additional data that can be used by the merge callback.

## -returns

Type: <b>const void*</b>

A pointer to constant data which results from the merge, or <b>NULL</b> if there is a failure when DPAMM_MERGE or DPAMM_INSERT is used.

## -see-also

<a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge">PFNDPAMERGE</a>
