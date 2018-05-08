---
UID: NS:commctrl._NM_UPDOWN
title: "_NM_UPDOWN"
author: windows-driver-content
description: Contains information specific to up-down control notification messages. It is identical to and replaces the NM_UPDOWN structure.
old-location: controls\NMUPDOWN.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\updown\structures\nmupdown.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: "*LPNMUPDOWN, LPNMUPDOWN, LPNMUPDOWN structure pointer [Windows Controls], NMUPDOWN, NMUPDOWN structure [Windows Controls], _NM_UPDOWN, _win32_NMUPDOWN, _win32_NMUPDOWN_cpp, commctrl/LPNMUPDOWN, commctrl/NMUPDOWN, controls.NMUPDOWN, controls._win32_NMUPDOWN"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: NMUPDOWN, *LPNMUPDOWN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMUPDOWN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _NM_UPDOWN structure


## -description


Contains information specific to up-down control notification messages. It is identical to and replaces the 
			<b>NM_UPDOWN</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field iPos

Type: <b>int</b>

Signed integer value that represents the up-down control's current position. 


### -field iDelta

Type: <b>int</b>

Signed integer value that represents the proposed change in the up-down control's position. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/66262566-d35a-4b2a-8157-d1e789a21016">UDN_DELTAPOS</a>



<a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a>
 

 

