---
UID: NF:commctrl.TabCtrl_HitTest
title: TabCtrl_HitTest macro (commctrl.h)
description: Determines which tab, if any, is at a specified screen position. You can use this macro or send the TCM_HITTEST message explicitly.helpviewer_keywords: ["TabCtrl_HitTest","TabCtrl_HitTest macro [Windows Controls]","_win32_TabCtrl_HitTest","_win32_TabCtrl_HitTest_cpp","commctrl/TabCtrl_HitTest","controls.TabCtrl_HitTest","controls._win32_TabCtrl_HitTest"]
old-location: controls\TabCtrl_HitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_hittest.htm
ms.date: 12/05/2018
ms.keywords: TabCtrl_HitTest, TabCtrl_HitTest macro [Windows Controls], _win32_TabCtrl_HitTest, _win32_TabCtrl_HitTest_cpp, commctrl/TabCtrl_HitTest, controls.TabCtrl_HitTest, controls._win32_TabCtrl_HitTest
f1_keywords:
- commctrl/TabCtrl_HitTest
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
- TabCtrl_HitTest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TabCtrl_HitTest macro


## -description


Determines which tab, if any, is at a specified screen position. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tcm-hittest">TCM_HITTEST</a> message explicitly. 


## -parameters




### -param hwndTC

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control. 


### -param pinfo

Type: <b>LPTCHITTESTINFO</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tchittestinfo">TCHITTESTINFO</a> structure that specifies the screen position to test. 

