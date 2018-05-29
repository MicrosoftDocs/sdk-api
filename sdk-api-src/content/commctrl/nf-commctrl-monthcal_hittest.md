---
UID: NF:commctrl.MonthCal_HitTest
title: MonthCal_HitTest macro
author: windows-sdk-content
description: Determines which portion of a month calendar control is at a given point on the screen. You can use this macro or send the MCM_HITTEST message explicitly.
old-location: controls\MonthCal_HitTest.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_hittest.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MonthCal_HitTest, MonthCal_HitTest macro [Windows Controls], _win32_MonthCal_HitTest, _win32_MonthCal_HitTest_cpp, commctrl/MonthCal_HitTest, controls.MonthCal_HitTest, controls._win32_MonthCal_HitTest
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	MonthCal_HitTest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_HitTest macro


## -description


Determines which portion of a month calendar control is at a given point on the screen. You can use this macro or send the <a href="https://msdn.microsoft.com/51e74b07-4ed7-488d-ad5d-116f046577fc">MCM_HITTEST</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param pinfo

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - pMCHitTest

Type: <b>PMCHITTESTINFO</b>

Pointer to an <a href="https://msdn.microsoft.com/82597f85-25c9-416a-b9b9-fee84f7480d7">MCHITTESTINFO</a> structure. Upon calling the macro, the <b>cbSize</b> member must be set to the size of the <b>MCHITTESTINFO</b> structure, and <b>pt</b> must be set to the point you want to hit test. 

