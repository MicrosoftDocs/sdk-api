---
UID: NF:commctrl.MonthCal_HitTest
title: MonthCal_HitTest macro (commctrl.h)
description: Determines which portion of a month calendar control is at a given point on the screen. You can use this macro or send the MCM_HITTEST message explicitly.helpviewer_keywords: ["MonthCal_HitTest","MonthCal_HitTest macro [Windows Controls]","_win32_MonthCal_HitTest","_win32_MonthCal_HitTest_cpp","commctrl/MonthCal_HitTest","controls.MonthCal_HitTest","controls._win32_MonthCal_HitTest"]
old-location: controls\MonthCal_HitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_hittest.htm
ms.date: 12/05/2018
ms.keywords: MonthCal_HitTest, MonthCal_HitTest macro [Windows Controls], _win32_MonthCal_HitTest, _win32_MonthCal_HitTest_cpp, commctrl/MonthCal_HitTest, controls.MonthCal_HitTest, controls._win32_MonthCal_HitTest
f1_keywords:
- commctrl/MonthCal_HitTest
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
- MonthCal_HitTest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_HitTest macro


## -description


Determines which portion of a month calendar control is at a given point on the screen. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-hittest">MCM_HITTEST</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


### -param pinfo

Type: <b>PMCHITTESTINFO</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-mchittestinfo">MCHITTESTINFO</a> structure. Upon calling the macro, the <b>cbSize</b> member must be set to the size of the <b>MCHITTESTINFO</b> structure, and <b>pt</b> must be set to the point you want to hit test. 

