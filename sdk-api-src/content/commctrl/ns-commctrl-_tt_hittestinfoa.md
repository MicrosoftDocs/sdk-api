---
UID: NS:commctrl._TT_HITTESTINFOA
title: "_TT_HITTESTINFOA"
author: windows-sdk-content
description: Contains information that a tooltip control uses to determine whether a point is in the bounding rectangle of the specified tool. If the point is in the rectangle, the structure receives information about the tool.
old-location: controls\TTHITTESTINFO.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\tthittestinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPTTHITTESTINFOA, LPHITTESTINFO, LPHITTESTINFO structure pointer [Windows Controls], TTHITTESTINFO, TTHITTESTINFO structure [Windows Controls], TTHITTESTINFOA, TTHITTESTINFOW, _TT_HITTESTINFOA, _win32_TTHITTESTINFO, _win32_TTHITTESTINFO_cpp, commctrl/LPHITTESTINFO, commctrl/TTHITTESTINFO, commctrl/TTHITTESTINFOA, commctrl/TTHITTESTINFOW, controls.TTHITTESTINFO, controls._win32_TTHITTESTINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TTHITTESTINFOW (Unicode) and TTHITTESTINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TTHITTESTINFOA, *LPTTHITTESTINFOA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TTHITTESTINFO
 - TTHITTESTINFOA
 - TTHITTESTINFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _TT_HITTESTINFOA structure


## -description


Contains information that a tooltip control uses to determine whether a point is in the bounding rectangle of the specified tool. If the point is in the rectangle, the structure receives information about the tool. 


## -struct-fields




### -field hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tool or window with the specified tool. 


### -field pt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

Client coordinates of the point to test. 


### -field ti

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb760256(v=VS.85).aspx">TOOLINFO</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb760256(v=VS.85).aspx">TOOLINFO</a> structure. If the point specified by 
					<b>pt</b> is in the tool specified by 
					<b>hwnd</b>, this structure receives information about the tool. The 
					<b>cbSize</b> member of this structure must be filled in before sending this message. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb760399(v=VS.85).aspx">TTM_HITTEST</a> message. 



