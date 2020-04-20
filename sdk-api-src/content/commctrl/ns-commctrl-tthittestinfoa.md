---
UID: NS:commctrl._TT_HITTESTINFOA
title: TTHITTESTINFOA (commctrl.h)
description: Contains information that a tooltip control uses to determine whether a point is in the bounding rectangle of the specified tool. If the point is in the rectangle, the structure receives information about the tool.helpviewer_keywords: ["*LPTTHITTESTINFOA","LPHITTESTINFO","LPHITTESTINFO structure pointer [Windows Controls]","TTHITTESTINFO","TTHITTESTINFO structure [Windows Controls]","TTHITTESTINFOA","TTHITTESTINFOW","_win32_TTHITTESTINFO","_win32_TTHITTESTINFO_cpp","commctrl/LPHITTESTINFO","commctrl/TTHITTESTINFO","commctrl/TTHITTESTINFOA","commctrl/TTHITTESTINFOW","controls.TTHITTESTINFO","controls._win32_TTHITTESTINFO"]
old-location: controls\TTHITTESTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\tthittestinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPTTHITTESTINFOA, LPHITTESTINFO, LPHITTESTINFO structure pointer [Windows Controls], TTHITTESTINFO, TTHITTESTINFO structure [Windows Controls], TTHITTESTINFOA, TTHITTESTINFOW, _win32_TTHITTESTINFO, _win32_TTHITTESTINFO_cpp, commctrl/LPHITTESTINFO, commctrl/TTHITTESTINFO, commctrl/TTHITTESTINFOA, commctrl/TTHITTESTINFOW, controls.TTHITTESTINFO, controls._win32_TTHITTESTINFO'
f1_keywords:
- commctrl/TTHITTESTINFO
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
req.unicode-ansi: TTHITTESTINFOW (Unicode) and TTHITTESTINFOA (ANSI)
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
- TTHITTESTINFO
- TTHITTESTINFOA
- TTHITTESTINFOW
targetos: Windows
req.typenames: TTHITTESTINFOA, *LPTTHITTESTINFOA
req.redist: 
ms.custom: 19H1
---

# TTHITTESTINFOA structure


## -description


Contains information that a tooltip control uses to determine whether a point is in the bounding rectangle of the specified tool. If the point is in the rectangle, the structure receives information about the tool. 


## -struct-fields




### -field hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tool or window with the specified tool. 


### -field pt

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a></b>

Client coordinates of the point to test. 


### -field ti

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa">TOOLINFO</a></b>


<a href="https://docs.microsoft.com/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa">TOOLINFO</a> structure. If the point specified by 
					<b>pt</b> is in the tool specified by 
					<b>hwnd</b>, this structure receives information about the tool. The 
					<b>cbSize</b> member of this structure must be filled in before sending this message. 


## -remarks



This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/Controls/ttm-hittest">TTM_HITTEST</a> message. 



