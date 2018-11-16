---
UID: NF:shlobj_core.DAD_DragEnterEx2
title: DAD_DragEnterEx2 function
author: windows-sdk-content
description: Locks updates to the specified window during a drag-and-drop operation and displays the drag image at the specified position within the window.
old-location: shell\DAD_DragEnterEx2.htm
tech.root: shell
ms.assetid: d9d902c5-c488-4e23-a749-bae42c6cb719
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DAD_DragEnterEx2, DAD_DragEnterEx2 function [Windows Shell], _shell_DAD_DragEnterEx2, shell.DAD_DragEnterEx2, shlobj_core/DAD_DragEnterEx2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - DAD_DragEnterEx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DAD_DragEnterEx2
: 
---

# DAD_DragEnterEx2 function


## -description


<p class="CCE_Message">[<b>DAD_DragEnterEx2</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/en-us/library/Bb761526(v=VS.85).aspx">ImageList_DragEnter</a> instead.]

Locks updates to the specified window during a drag-and-drop operation and displays the drag image at the specified position within the window.


## -parameters




### -param hwndTarget [in]

Type: <b>HWND</b>

A handle to the window that owns the drag image.


### -param ptStart

Type: <b>const <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

Specifies the coordinates at which to begin displaying the drag image. The coordinates are relative to the upper-left corner of the window, not the client area.


### -param pdtObject [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object. This data object contains the data being transferred in the drag-and-drop operation. If the drop occurs, this data object will be incorporated into the target. This parameter may be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/32f98df7-e357-4d17-9e33-f162a6ffb7ed">DAD_DragEnterEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761526(v=VS.85).aspx">ImageList_DragEnter</a>
 

 

