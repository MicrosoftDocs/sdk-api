---
UID: NS:commctrl.tagNMTTCUSTOMDRAW
title: NMTTCUSTOMDRAW (commctrl.h)
author: windows-sdk-content
description: Contains information specific to an NM_CUSTOMDRAW notification code sent by a tooltip control.
old-location: controls\NMTTCUSTOMDRAW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\nmttcustomdraw.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMTTCUSTOMDRAW, LPNMTTCUSTOMDRAW, LPNMTTCUSTOMDRAW structure pointer [Windows Controls], NMTTCUSTOMDRAW, NMTTCUSTOMDRAW structure [Windows Controls], _win32_NMTTCUSTOMDRAW, _win32_NMTTCUSTOMDRAW_cpp, commctrl/LPNMTTCUSTOMDRAW, commctrl/NMTTCUSTOMDRAW, controls.NMTTCUSTOMDRAW, controls._win32_NMTTCUSTOMDRAW"
ms.topic: struct
f1_keywords: 
 - "commctrl/NMTTCUSTOMDRAW"
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
 - NMTTCUSTOMDRAW
product: Windows
targetos: Windows
req.typenames: NMTTCUSTOMDRAW, *LPNMTTCUSTOMDRAW
req.redist: 
ms.custom: 19H1
---

# NMTTCUSTOMDRAW structure


## -description


Contains information specific to an <a href="https://docs.microsoft.com/windows/desktop/Controls/nm-customdraw-tooltip">NM_CUSTOMDRAW</a> notification code sent by a tooltip control. 


## -struct-fields




### -field nmcd

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw">NMCUSTOMDRAW</a></b>

Contains general custom draw information. 


### -field uDrawFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies how tooltip text will be formatted when it is displayed. An application may change this field to alter the way text is drawn. This value is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-drawtext">DrawText</a> function internally. All values for the 
					<i>uFormat</i> parameter of <b>DrawText</b> are valid. 

