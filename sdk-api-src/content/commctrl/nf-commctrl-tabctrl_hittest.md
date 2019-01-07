---
UID: NF:commctrl.TabCtrl_HitTest
title: TabCtrl_HitTest macro
author: windows-sdk-content
description: Determines which tab, if any, is at a specified screen position. You can use this macro or send the TCM_HITTEST message explicitly.
old-location: controls\TabCtrl_HitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_hittest.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TabCtrl_HitTest, TabCtrl_HitTest macro [Windows Controls], _win32_TabCtrl_HitTest, _win32_TabCtrl_HitTest_cpp, commctrl/TabCtrl_HitTest, controls.TabCtrl_HitTest, controls._win32_TabCtrl_HitTest
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_HitTest macro


## -description


Determines which tab, if any, is at a specified screen position. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760604(v=VS.85).aspx">TCM_HITTEST</a> message explicitly. 


## -parameters




### -param hwndTC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param pinfo

Type: <b>LPTCHITTESTINFO</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb760553(v=VS.85).aspx">TCHITTESTINFO</a> structure that specifies the screen position to test. 

