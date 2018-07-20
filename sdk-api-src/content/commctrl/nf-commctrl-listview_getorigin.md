---
UID: NF:commctrl.ListView_GetOrigin
title: ListView_GetOrigin macro
author: windows-sdk-content
description: Gets the current view origin for a list-view control. You can use this macro or send the LVM_GETORIGIN message explicitly.
old-location: controls\ListView_GetOrigin.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getorigin.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ListView_GetOrigin, ListView_GetOrigin macro [Windows Controls], _win32_ListView_GetOrigin, _win32_ListView_GetOrigin_cpp, commctrl/ListView_GetOrigin, controls.ListView_GetOrigin, controls._win32_ListView_GetOrigin
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
 - ListView_GetOrigin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetOrigin macro


## -description


Gets the current view origin for a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761063(v=VS.85).aspx">LVM_GETORIGIN</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param ppt

TBD






#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - lpptOrg

Type: <b>LPPOINT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that receives the view origin. 

