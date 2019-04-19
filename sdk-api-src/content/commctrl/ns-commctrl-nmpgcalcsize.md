---
UID: NS:commctrl.__unnamed_struct_17
title: NMPGCALCSIZE (commctrl.h)
author: windows-sdk-content
description: Contains and receives information that the pager control uses to calculate the scrollable area of the contained window. It is used with the PGN_CALCSIZE notification.
old-location: controls\NMPGCALCSIZE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\structures\nmpgcalcsize.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMPGCALCSIZE, LPNMPGCALCSIZE, LPNMPGCALCSIZE structure pointer [Windows Controls], NMPGCALCSIZE, NMPGCALCSIZE structure [Windows Controls], PGF_CALCHEIGHT, PGF_CALCWIDTH, _win32_NMPGCALCSIZE, _win32_NMPGCALCSIZE_cpp, commctrl/LPNMPGCALCSIZE, commctrl/NMPGCALCSIZE, controls.NMPGCALCSIZE, controls._win32_NMPGCALCSIZE"
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
 - NMPGCALCSIZE
product: Windows
targetos: Windows
req.typenames: NMPGCALCSIZE, *LPNMPGCALCSIZE
req.redist: 
ms.custom: 19H1
---

# NMPGCALCSIZE structure


## -description


Contains and receives information that the pager control uses to calculate the scrollable area of the contained window. It is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb760864(v=VS.85).aspx">PGN_CALCSIZE</a> notification. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about the notification. 


### -field dwFlag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Value that indicates which dimension is being requested. This will be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PGF_CALCHEIGHT"></a><a id="pgf_calcheight"></a><dl>
<dt><b>PGF_CALCHEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The height of the scrollable area is being requested. The height must be placed in the 
						<b>iHeight</b> member before returning from the notification. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGF_CALCWIDTH"></a><a id="pgf_calcwidth"></a><dl>
<dt><b>PGF_CALCWIDTH</b></dt>
</dl>
</td>
<td width="60%">
The width of the scrollable area is being requested. The width must be placed in the 
						<b>iWidth</b> member before returning from the notification. 

</td>
</tr>
</table>
 


### -field iWidth

Type: <b>int</b>

Receives the desired width of the scrollable area, in pixels. 


### -field iHeight

Type: <b>int</b>

Receives the desired height of the scrollable area, in pixels. 

