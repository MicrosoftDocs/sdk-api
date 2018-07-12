---
UID: NF:commctrl.ListView_SetGroupInfo
title: ListView_SetGroupInfo macro
author: windows-sdk-content
description: Sets group information. You can use this macro or send the LVM_SETGROUPINFO message explicitly.
old-location: controls\ListView_SetGroupInfo.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupinfo.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ListView_SetGroupInfo, ListView_SetGroupInfo macro [Windows Controls], _win32_ListView_SetGroupInfo, _win32_ListView_SetGroupInfo_cpp, commctrl/ListView_SetGroupInfo, controls.ListView_SetGroupInfo, controls._win32_ListView_SetGroupInfo
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_SetGroupInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetGroupInfo macro


## -description


Sets group information. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761167(v=VS.85).aspx">LVM_SETGROUPINFO</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iGroupId

Type: <b>int</b>


### -param pgrp

Type: <b>PLVGROUP</b>

<a href="https://msdn.microsoft.com/library/Bb774769(v=VS.85).aspx">LVGROUP</a>

## -remarks



To use <b>ListView_SetGroupInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



