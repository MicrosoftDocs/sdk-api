---
UID: NS:commctrl._NM_UPDOWN
title: NMUPDOWN (commctrl.h)
author: windows-sdk-content
description: Contains information specific to up-down control notification messages. It is identical to and replaces the NM_UPDOWN structure.
old-location: controls\NMUPDOWN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\updown\structures\nmupdown.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMUPDOWN, LPNMUPDOWN, LPNMUPDOWN structure pointer [Windows Controls], NMUPDOWN, NMUPDOWN structure [Windows Controls], _win32_NMUPDOWN, _win32_NMUPDOWN_cpp, commctrl/LPNMUPDOWN, commctrl/NMUPDOWN, controls.NMUPDOWN, controls._win32_NMUPDOWN"
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
 - NMUPDOWN
product: Windows
targetos: Windows
req.typenames: NMUPDOWN, *LPNMUPDOWN
req.redist: 
ms.custom: 19H1
---

# NMUPDOWN structure


## -description


Contains information specific to up-down control notification messages. It is identical to and replaces the 
			<b>NM_UPDOWN</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-_nmhdr">NMHDR</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-_nmhdr">NMHDR</a> structure that contains additional information about the notification. 


### -field iPos

Type: <b>int</b>

Signed integer value that represents the up-down control's current position. 


### -field iDelta

Type: <b>int</b>

Signed integer value that represents the proposed change in the up-down control's position. 


## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/udn-deltapos">UDN_DELTAPOS</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>
 

 

