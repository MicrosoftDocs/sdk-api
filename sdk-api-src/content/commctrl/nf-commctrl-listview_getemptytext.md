---
UID: NF:commctrl.ListView_GetEmptyText
title: ListView_GetEmptyText macro
author: windows-sdk-content
description: Gets the text meant for display when the list-view control appears empty. Use this macro or send the LVM_GETEMPTYTEXT message explicitly.
old-location: controls\ListView_GetEmptyText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getemptytext.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ListView_GetEmptyText, ListView_GetEmptyText macro [Windows Controls], _shell_ListView_GetEmptyText, _shell_ListView_GetEmptyText_cpp, commctrl/ListView_GetEmptyText, controls.ListView_GetEmptyText, controls._shell_ListView_GetEmptyText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ListView_GetEmptyText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetEmptyText macro


## -description


Gets the text meant for display when the list-view control appears empty. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774921(v=VS.85).aspx">LVM_GETEMPTYTEXT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param pszText [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

A pointer to a null-terminated, Unicode buffer of size specified by <i>cchText</i> to receive the text. The caller is responsible for allocating the buffer.


### -param cchText [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of the buffer pointed to by <i>pszText</i>, including the terminating               <b>NULL</b>.

