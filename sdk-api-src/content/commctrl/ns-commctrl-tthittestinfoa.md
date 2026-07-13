---
UID: NS:commctrl._TT_HITTESTINFOA
title: TTHITTESTINFOA (commctrl.h)
description: Contains information that a tooltip control uses to determine whether a point is in the bounding rectangle of the specified tool. If the point is in the rectangle, the structure receives information about the tool. (ANSI)
helpviewer_keywords: ["*LPTTHITTESTINFOA","LPHITTESTINFO","LPHITTESTINFO structure pointer [Windows Controls]","TTHITTESTINFO","TTHITTESTINFO structure [Windows Controls]","TTHITTESTINFOA","TTHITTESTINFOW","_win32_TTHITTESTINFO","_win32_TTHITTESTINFO_cpp","commctrl/LPHITTESTINFO","commctrl/TTHITTESTINFO","commctrl/TTHITTESTINFOA","commctrl/TTHITTESTINFOW","controls.TTHITTESTINFO","controls._win32_TTHITTESTINFO"]
old-location: controls\TTHITTESTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\tthittestinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPTTHITTESTINFOA, LPHITTESTINFO, LPHITTESTINFO structure pointer [Windows Controls], TTHITTESTINFO, TTHITTESTINFO structure [Windows Controls], TTHITTESTINFOA, TTHITTESTINFOW, _win32_TTHITTESTINFO, _win32_TTHITTESTINFO_cpp, commctrl/LPHITTESTINFO, commctrl/TTHITTESTINFO, commctrl/TTHITTESTINFOA, commctrl/TTHITTESTINFOW, controls.TTHITTESTINFO, controls._win32_TTHITTESTINFO'
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
targetos: Windows
req.typenames: TTHITTESTINFOA, *LPTTHITTESTINFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TT_HITTESTINFOA
 - commctrl/_TT_HITTESTINFOA
 - LPTTHITTESTINFOA
 - commctrl/LPTTHITTESTINFOA
 - TTHITTESTINFOA
 - commctrl/TTHITTESTINFOA
dev_langs:
 - c++
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
---

# TTHITTESTINFOA structure


## -description

Contains information that a tooltip control uses to determine whether a point is in the bounding rectangle of the specified tool. If the point is in the rectangle, the structure receives information about the tool.

## -struct-fields

### -field hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tool or window with the specified tool.

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

Client coordinates of the point to test.

### -field ti

Type: <b><a href="/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa">TOOLINFO</a></b>


<a href="/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa">TOOLINFO</a> structure. If the point specified by 
					<b>pt</b> is in the tool specified by 
					<b>hwnd</b>, this structure receives information about the tool. The 
					<b>cbSize</b> member of this structure must be filled in before sending this message.

## -remarks

This structure is used with the <a href="/windows/desktop/Controls/ttm-hittest">TTM_HITTEST</a> message. 




> [!NOTE]
> The commctrl.h header defines TTHITTESTINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
