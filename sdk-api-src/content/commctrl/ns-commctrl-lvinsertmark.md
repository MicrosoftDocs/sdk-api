---
UID: NS:commctrl.LVINSERTMARK
title: LVINSERTMARK
author: windows-sdk-content
description: Used to describe insertion points.
old-location: controls\LVINSERTMARK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvinsertmark.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*LPLVINSERTMARK, LVIM_AFTER, LVINSERTMARK, LVINSERTMARK structure [Windows Controls], PLVINSERTMARK, PLVINSERTMARK structure pointer [Windows Controls], commctrl/LVINSERTMARK, commctrl/PLVINSERTMARK, controls.LVINSERTMARK, controls.inet_LVINSERTMARK, inet_LVINSERTMARK, inet_LVINSERTMARK_cpp"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
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
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - LVINSERTMARK
product: Windows
targetos: Windows
req.typenames: LVINSERTMARK, *LPLVINSERTMARK
req.redist: 
---

# LVINSERTMARK structure


## -description


Used to describe insertion points.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the <b>LVINSERTMARK</b> structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Flag that specifies where the insertion point should appear. Use the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVIM_AFTER"></a><a id="lvim_after"></a><dl>
<dt><b>LVIM_AFTER</b></dt>
</dl>
</td>
<td width="60%">
The insertion point appears after the item specified if the LVIM_AFTER flag is set; otherwise it appears before the specified item.

</td>
</tr>
</table>
 


### -field iItem

Type: <b>int</b>

Item next to which the insertion point appears. If this member contains -1, there is no insertion point.


### -field dwReserved

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

