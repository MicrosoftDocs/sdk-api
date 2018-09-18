---
UID: NC:dpa_dsa.PFNDPAMERGE
title: PFNDPAMERGE
author: windows-sdk-content
description: Defines the prototype for the merge function used by DPA_Merge.
old-location: controls\PFNDPAMERGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndpamerge.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DPAMM_DELETE, DPAMM_INSERT, DPAMM_MERGE, PFNDPAMERGE, PFNDPAMERGE callback, PFNDPAMERGE callback function [Windows Controls], _shell_PFNDPAMERGE, _shell_PFNDPAMERGE_cpp, controls.PFNDPAMERGE, controls._shell_PFNDPAMERGE, dpa_dsa/PFNDPAMERGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dpa_dsa.h
api_name:
 - PFNDPAMERGE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNDPAMERGE callback function


## -description


Defines the prototype for the merge function used by <a href="https://msdn.microsoft.com/c2d8ffab-1cd1-4328-9740-524c39b6821c">DPA_Merge</a>.


## -parameters




### -param uMsg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

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
Perform any additional processing needed when merging <i>pvSrc</i> into <i>pvDest</i>. The function should return a pointer to an item that contains the result of the merge. The value returned by the merge function is stored into the destination, which overwrites the previous value. If the merge function returns <b>NULL</b>, then the merge operation is abandoned.

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
Perform any user-defined processing when the merge results in an item being inserted as part of the merge. The return value of this function should point to the item result that is inserted as part of the merge. If the merge function returns <b>NULL</b>, then the merge operation is abandoned.

</td>
</tr>
</table>
 


### -param *pvDest [in]

Type: <b>void*</b>

A pointer to the first item in the merge.


### -param *pvSrc [in]

Type: <b>void*</b>

A pointer to the second item in the merge.


### -param lParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Additional data that can be used by the merge callback.


## -returns



A pointer to the item which results from the merge or <b>NULL</b> if there is a failure when <b>DPAMM_MERGE</b> or <b>DPAMM_INSERT</b> is used.




## -remarks



The callback function might not modify the dynamic pointer arrays (DPAs) involved in the merge operation.




## -see-also




<a href="https://msdn.microsoft.com/2ae5f250-c79e-4ca5-98c4-b15ed7d5b90a">PFNDPAMERGECONST</a>
 

 

