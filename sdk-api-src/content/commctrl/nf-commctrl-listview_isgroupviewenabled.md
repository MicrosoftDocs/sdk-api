---
UID: NF:commctrl.ListView_IsGroupViewEnabled
title: ListView_IsGroupViewEnabled macro (commctrl.h)
author: windows-sdk-content
description: Checks whether the list-view control has group view enabled. You can use this macro or send the LVM_ISGROUPVIEWENABLED message explicitly.
old-location: controls\ListView_IsGroupViewEnabled.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_isgroupviewenabled.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_IsGroupViewEnabled, ListView_IsGroupViewEnabled macro [Windows Controls], _win32_ListView_IsGroupViewEnabled, _win32_ListView_IsGroupViewEnabled_cpp, commctrl/ListView_IsGroupViewEnabled, controls.ListView_IsGroupViewEnabled, controls._win32_ListView_IsGroupViewEnabled
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
 - ListView_IsGroupViewEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_IsGroupViewEnabled macro


## -description


Checks whether the list-view control has group view
 enabled. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761133(v=VS.85).aspx">LVM_ISGROUPVIEWENABLED</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_IsGroupViewEnabled</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



