---
UID: NS:commctrl._UDACCEL
title: UDACCEL (commctrl.h)
author: windows-sdk-content
description: Contains acceleration information for an up-down control.
old-location: controls\UDACCEL.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\updown\structures\udaccel.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPUDACCEL, LPUDACCEL, LPUDACCEL structure pointer [Windows Controls], UDACCEL, UDACCEL structure [Windows Controls], _win32_UDACCEL, _win32_UDACCEL_cpp, commctrl/LPUDACCEL, commctrl/UDACCEL, controls.UDACCEL, controls._win32_UDACCEL"
ms.topic: struct
f1_keywords: 
 - "commctrl/UDACCEL"
dev_langs:
 - c++
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
 - UDACCEL
targetos: Windows
req.typenames: UDACCEL, *LPUDACCEL
req.redist: 
ms.custom: 19H1
---

# UDACCEL structure


## -description


Contains acceleration information for an up-down control. 


## -struct-fields




### -field nSec

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Amount of elapsed time, in seconds, before the position change increment specified by 
					<b>nInc</b> is used. 


### -field nInc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Position change increment to use after the time specified by 
					<b>nSec</b> elapses. 

