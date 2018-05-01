---
UID: NF:commctrl.ListView_GetGroupMetrics
title: ListView_GetGroupMetrics macro
author: windows-driver-content
description: Gets information about the display of groups. You can use this macro or send the LVM_GETGROUPMETRICS message explicitly.
old-location: controls\ListView_GetGroupMetrics.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupmetrics.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ListView_GetGroupMetrics, ListView_GetGroupMetrics macro [Windows Controls], _win32_ListView_GetGroupMetrics, _win32_ListView_GetGroupMetrics_cpp, commctrl/ListView_GetGroupMetrics, controls.ListView_GetGroupMetrics, controls._win32_ListView_GetGroupMetrics
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ListView_GetGroupMetrics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetGroupMetrics macro


## -description


Gets information about the display of groups. You can use this macro or send the <a href="https://msdn.microsoft.com/75e7da66-50c6-4834-ae66-e43b8f9b0b34">LVM_GETGROUPMETRICS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pGroupMetrics

Type: <b>PLVGROUPMETRICS</b>

<a href="https://msdn.microsoft.com/8cbe72d0-7d99-48fb-b10b-bc862ba93f6e">LVGROUPMETRICS</a>

## -remarks



To use <b>ListView_GetGroupMetrics</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



