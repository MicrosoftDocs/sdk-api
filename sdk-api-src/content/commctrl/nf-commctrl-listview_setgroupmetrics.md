---
UID: NF:commctrl.ListView_SetGroupMetrics
title: ListView_SetGroupMetrics macro
author: windows-sdk-content
description: Sets information about the display of groups. You can use this macro or send the LVM_SETGROUPMETRICS message explicitly.
old-location: controls\ListView_SetGroupMetrics.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupmetrics.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ListView_SetGroupMetrics, ListView_SetGroupMetrics macro [Windows Controls], _win32_ListView_SetGroupMetrics, _win32_ListView_SetGroupMetrics_cpp, commctrl/ListView_SetGroupMetrics, controls.ListView_SetGroupMetrics, controls._win32_ListView_SetGroupMetrics
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
 - ListView_SetGroupMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetGroupMetrics macro


## -description


Sets information about the display of groups. You can use this macro or send the <a href="https://msdn.microsoft.com/268b478d-da1f-4efe-9ee9-af3f12e089ee">LVM_SETGROUPMETRICS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pGroupMetrics

Type: <b>PLVGROUPMETRICS</b>

<a href="https://msdn.microsoft.com/8cbe72d0-7d99-48fb-b10b-bc862ba93f6e">LVGROUPMETRICS</a>

## -remarks



To use <b>ListView_SetGroupMetrics</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



