---
UID: NS:commctrl.tagNMPGHOTITEM
title: tagNMPGHOTITEM
author: windows-sdk-content
description: Contains information used with the PGN_HOTITEMCHANGE notification code.
old-location: controls\NMPGHOTITEM.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\pager\structures\nmpghotitem.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPNMPGHOTITEM, LPNMPGHOTITEM, LPNMPGHOTITEM structure pointer [Windows Controls], NMPGHOTITEM, NMPGHOTITEM structure [Windows Controls], commctrl/LPNMPGHOTITEM, commctrl/NMPGHOTITEM, controls.NMPGHOTITEM, controls.inet_NMPGHOTITEM, inet_NMPGHOTITEM, inet_NMPGHOTITEM_cpp, tagNMPGHOTITEM"
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
tech.root: 
req.typenames: NMPGHOTITEM, *LPNMPGHOTITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMPGHOTITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMPGHOTITEM structure


## -description


Contains information used with the <a href="https://msdn.microsoft.com/library/Bb760865(v=VS.85).aspx">PGN_HOTITEMCHANGE</a> notification code. 



## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field idOld

Type: <b>int</b>

Value of type <b>int</b> that specifies the command identifier of the previously highlighted item. 


### -field idNew

Type: <b>int</b>

Value of type <b>int</b> that specifies the command identifier of the highlighted item. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>DWORD</b> that contains flags that indicate why the hot item has changed. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>HICF_ENTERING</dt>
</dl>
</td>
<td width="60%">
If this flag is set, there is no previous hot item and <b>idOld</b> does not contain valid information.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>HICF_LEAVING</dt>
</dl>
</td>
<td width="60%">
If this flag is set, there is no new hot item and <b>idNew</b> does not contain valid information.

</td>
</tr>
</table>
 

