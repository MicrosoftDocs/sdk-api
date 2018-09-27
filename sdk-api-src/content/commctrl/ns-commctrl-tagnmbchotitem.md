---
UID: NS:commctrl.tagNMBCHOTITEM
title: tagNMBCHOTITEM
author: windows-sdk-content
description: Contains information about the movement of the mouse over a button control.
old-location: controls\NMBCHOTITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonstructures\nmbchotitem.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*LPNMBCHOTITEM, HICF_ENTERING, HICF_LEAVING, LPNMBCHOTITEM, LPNMBCHOTITEM structure pointer [Windows Controls], NMBCHOTITEM, NMBCHOTITEM structure [Windows Controls], _win32_NMBCHOTITEM_str, _win32_NMBCHOTITEM_str_cpp, commctrl/LPNMBCHOTITEM, commctrl/NMBCHOTITEM, controls.NMBCHOTITEM, controls._win32_NMBCHOTITEM_str, tagNMBCHOTITEM"
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
 - NMBCHOTITEM
product: Windows
targetos: Windows
req.typenames: NMBCHOTITEM, *LPNMBCHOTITEM
req.redist: 
---

# tagNMBCHOTITEM structure


## -description


Contains information about the movement of the mouse over a button control.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The action of the mouse. This parameter can be one of the following values combined with HICF_MOUSE. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HICF_ENTERING"></a><a id="hicf_entering"></a><dl>
<dt><b>HICF_ENTERING</b></dt>
</dl>
</td>
<td width="60%">
The mouse is entering the button.

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_LEAVING"></a><a id="hicf_leaving"></a><dl>
<dt><b>HICF_LEAVING</b></dt>
</dl>
</td>
<td width="60%">
The mouse is leaving the button.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775984(v=VS.85).aspx">BCN_HOTITEMCHANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775943(v=VS.85).aspx">Buttons</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a>



<b>Reference</b>
 

 

