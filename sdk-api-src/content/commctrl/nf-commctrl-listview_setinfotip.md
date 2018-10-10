---
UID: NF:commctrl.ListView_SetInfoTip
title: ListView_SetInfoTip macro
author: windows-sdk-content
description: Sets tooltip text. You can use this macro or send the LVM_SETINFOTIP message explicitly.
old-location: controls\ListView_SetInfoTip.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setinfotip.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ListView_SetInfoTip, ListView_SetInfoTip macro [Windows Controls], _win32_ListView_SetInfoTip, _win32_ListView_SetInfoTip_cpp, commctrl/ListView_SetInfoTip, controls.ListView_SetInfoTip, controls._win32_ListView_SetInfoTip
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
 - ListView_SetInfoTip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetInfoTip macro


## -description


Sets tooltip text. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761180(v=VS.85).aspx">LVM_SETINFOTIP</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param plvInfoTip

Type: <b>PLVSETINFOTIP</b>

<a href="https://msdn.microsoft.com/en-us/library/Bb774764(v=VS.85).aspx">LVSETINFOTIP</a>

## -remarks



To use <b>ListView_SetInfoTip</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



