---
UID: NF:commctrl.ListView_GetGroupMetrics
title: ListView_GetGroupMetrics macro
author: windows-sdk-content
description: Gets information about the display of groups. You can use this macro or send the LVM_GETGROUPMETRICS message explicitly.
old-location: controls\ListView_GetGroupMetrics.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupmetrics.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
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
 - ListView_GetGroupMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetGroupMetrics macro


## -description


Gets information about the display of groups. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774934(v=VS.85).aspx">LVM_GETGROUPMETRICS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pGroupMetrics

Type: <b>PLVGROUPMETRICS</b>

<a href="https://msdn.microsoft.com/en-us/library/Bb774752(v=VS.85).aspx">LVGROUPMETRICS</a>

## -remarks



To use <b>ListView_GetGroupMetrics</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



