---
UID: NS:winuser.tagCBT_CREATEWNDA
title: tagCBT_CREATEWNDA
author: windows-sdk-content
description: Contains information passed to a WH_CBT hook procedure, CBTProc, before a window is created.
old-location: winmsg\cbt_createwnd.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\cbt_createwnd.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPCBT_CREATEWNDA, CBT_CREATEWND, CBT_CREATEWND structure [Windows and Messages], CBT_CREATEWNDA, CBT_CREATEWNDW, LPCBT_CREATEWND, LPCBT_CREATEWND structure pointer [Windows and Messages], _win32_CBT_CREATEWND_str, _win32_cbt_createwnd_str_cpp, tagCBT_CREATEWNDA, winmsg.cbt_createwnd, winui._win32_cbt_createwnd_str, winuser/CBT_CREATEWND, winuser/CBT_CREATEWNDA, winuser/CBT_CREATEWNDW, winuser/LPCBT_CREATEWND"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CBT_CREATEWNDW (Unicode) and CBT_CREATEWNDA (ANSI)
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
 - Winuser.h
api_name:
 - CBT_CREATEWND
 - CBT_CREATEWNDA
 - CBT_CREATEWNDW
product: Windows
targetos: Windows
req.typenames: CBT_CREATEWNDA, *LPCBT_CREATEWNDA
req.redist: 
---

# tagCBT_CREATEWNDA structure


## -description


Contains information passed to a <b>WH_CBT</b> hook procedure, <a href="https://msdn.microsoft.com/26c48395-f0b8-4c03-bf65-d76cdf0117d6">CBTProc</a>, before a window is created. 


## -struct-fields




### -field lpcs

Type: <b>LPCREATESTRUCT</b>

A pointer to a <a href="https://msdn.microsoft.com/2d67fed4-43de-4151-b124-b710ea64e8a6">CREATESTRUCT</a> structure that contains initialization parameters for the window about to be created. 


### -field hwndInsertAfter

Type: <b>HWND</b>

A handle to the window whose position in the Z order precedes that of the window being created. This member can also be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/26c48395-f0b8-4c03-bf65-d76cdf0117d6">CBTProc</a>



<a href="https://msdn.microsoft.com/2d67fed4-43de-4151-b124-b710ea64e8a6">CREATESTRUCT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/987095d7-059f-4eae-925d-6723ab6d524c">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/66c96282-528c-4f57-acab-ae03178e4fe9">SetWindowsHookEx</a>
 

 

