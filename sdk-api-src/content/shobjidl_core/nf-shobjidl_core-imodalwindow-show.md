---
UID: NF:shobjidl_core.IModalWindow.Show
title: IModalWindow::Show
author: windows-sdk-content
description: Launches the modal window.
old-location: shell\IModalWindow_Show.htm
old-project: shell
ms.assetid: 0284b694-64d1-48db-bef3-92f808b29b23
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IModalWindow interface [Windows Shell],Show method, IModalWindow.Show, IModalWindow::Show, Show, Show method [Windows Shell], Show method [Windows Shell],IModalWindow interface, _win32_IModalWindow_Show, shell.IModalWindow_Show, shobjidl_core/IModalWindow::Show
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IModalWindow.Show
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IModalWindow::Show


## -description


Launches the modal window.


## -parameters




### -param hwndOwner [in, optional]

Type: <b>HWND</b>

The handle of the owner window. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/40e6f80d-a778-4d5f-bb1b-db294815f8b5">HRESULT_FROM_WIN32</a>(ERROR_CANCELLED)</b></dt>
</dl>
</td>
<td width="60%">
The user closed the window by cancelling the operation.

</td>
</tr>
</table>
 



