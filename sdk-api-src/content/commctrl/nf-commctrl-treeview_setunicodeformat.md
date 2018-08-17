---
UID: NF:commctrl.TreeView_SetUnicodeFormat
title: TreeView_SetUnicodeFormat macro
author: windows-sdk-content
description: Sets the Unicode character format flag for the control.
old-location: controls\TreeView_SetUnicodeFormat.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setunicodeformat.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TreeView_SetUnicodeFormat, TreeView_SetUnicodeFormat macro [Windows Controls], _win32_TreeView_SetUnicodeFormat, _win32_TreeView_SetUnicodeFormat_cpp, commctrl/TreeView_SetUnicodeFormat, controls.TreeView_SetUnicodeFormat, controls._win32_TreeView_SetUnicodeFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
 - TreeView_SetUnicodeFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetUnicodeFormat macro


## -description


Sets the Unicode character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773775(v=VS.85).aspx">TVM_SETUNICODEFORMAT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the control. 


### -param fUnicode

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines the character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773895(v=VS.85).aspx">TreeView_GetUnicodeFormat</a>
 

 

