---
UID: NS:commctrl.tagNMVIEWCHANGE
title: tagNMVIEWCHANGE
author: windows-driver-content
description: Stores information required to process the MCN_VIEWCHANGE notification code.
old-location: controls\NMVIEWCHANGE.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\structures\nmviewchange.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*LPNMVIEWCHANGE, LPNMVIEWCHANGE, LPNMVIEWCHANGE structure pointer [Windows Controls], MCMV_CENTURY, MCMV_DECADE, MCMV_MONTH, MCMV_YEAR, NMVIEWCHANGE, NMVIEWCHANGE structure [Windows Controls], _shell_NMVIEWCHANGE, _shell_NMVIEWCHANGE_cpp, commctrl/LPNMVIEWCHANGE, commctrl/NMVIEWCHANGE, controls.NMVIEWCHANGE, controls._shell_NMVIEWCHANGE, tagNMVIEWCHANGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
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
req.typenames: NMVIEWCHANGE, *LPNMVIEWCHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMVIEWCHANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMVIEWCHANGE structure


## -description


Stores information required to process the <a href="https://msdn.microsoft.com/ee35ac1d-9aeb-4d75-9cef-016487f23602">MCN_VIEWCHANGE</a> notification code.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification code.


### -field dwOldView

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Old view. One of the following constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCMV_MONTH"></a><a id="mcmv_month"></a><dl>
<dt><b>MCMV_MONTH</b></dt>
</dl>
</td>
<td width="60%">
Monthly view.

</td>
</tr>
<tr>
<td width="40%"><a id="MCMV_YEAR"></a><a id="mcmv_year"></a><dl>
<dt><b>MCMV_YEAR</b></dt>
</dl>
</td>
<td width="60%">
Annual view.

</td>
</tr>
<tr>
<td width="40%"><a id="MCMV_DECADE"></a><a id="mcmv_decade"></a><dl>
<dt><b>MCMV_DECADE</b></dt>
</dl>
</td>
<td width="60%">
Decade view.

</td>
</tr>
<tr>
<td width="40%"><a id="MCMV_CENTURY"></a><a id="mcmv_century"></a><dl>
<dt><b>MCMV_CENTURY</b></dt>
</dl>
</td>
<td width="60%">
Century view.

</td>
</tr>
</table>
 


### -field dwNewView

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

New view. One of the constants listed at <b>dwOldView</b>.

