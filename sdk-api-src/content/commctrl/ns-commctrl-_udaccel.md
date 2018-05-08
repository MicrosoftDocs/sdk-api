---
UID: NS:commctrl._UDACCEL
title: "_UDACCEL"
author: windows-driver-content
description: Contains acceleration information for an up-down control.
old-location: controls\UDACCEL.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\updown\structures\udaccel.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: "*LPUDACCEL, LPUDACCEL, LPUDACCEL structure pointer [Windows Controls], UDACCEL, UDACCEL structure [Windows Controls], _UDACCEL, _win32_UDACCEL, _win32_UDACCEL_cpp, commctrl/LPUDACCEL, commctrl/UDACCEL, controls.UDACCEL, controls._win32_UDACCEL"
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
req.typenames: UDACCEL, *LPUDACCEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	UDACCEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _UDACCEL structure


## -description


Contains acceleration information for an up-down control. 


## -struct-fields




### -field nSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Amount of elapsed time, in seconds, before the position change increment specified by 
					<b>nInc</b> is used. 


### -field nInc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Position change increment to use after the time specified by 
					<b>nSec</b> elapses. 

