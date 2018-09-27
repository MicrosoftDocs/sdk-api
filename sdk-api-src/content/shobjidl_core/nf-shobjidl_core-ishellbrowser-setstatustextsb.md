---
UID: NF:shobjidl_core.IShellBrowser.SetStatusTextSB
title: IShellBrowser::SetStatusTextSB
author: windows-sdk-content
description: Sets and displays status text about the in-place object in the container's frame-window status bar.
old-location: shell\IShellBrowser_SetStatusTextSB.htm
tech.root: shell
ms.assetid: d7dd9f17-41e4-4c04-981e-a0bfe7c53fcf
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IShellBrowser interface [Windows Shell],SetStatusTextSB method, IShellBrowser.SetStatusTextSB, IShellBrowser::SetStatusTextSB, SetStatusTextSB, SetStatusTextSB method [Windows Shell], SetStatusTextSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_SetStatusTextSB, shell.IShellBrowser_SetStatusTextSB, shobjidl_core/IShellBrowser::SetStatusTextSB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellBrowser.SetStatusTextSB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellBrowser::SetStatusTextSB


## -description


Sets and displays status text about the in-place object in the container's frame-window status bar.


## -parameters




### -param pszStatusText

TBD




#### - lpszStatusText

Type: <b>LPCWSTR</b>

A pointer to a null-terminated character string that contains the message to display.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is also possible to send messages directly to the status window by using the <a href="https://msdn.microsoft.com/4494870b-45a8-478a-807a-7ed3674f69f3">IShellBrowser::SendControlMsg</a> method.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Use this method to set the contents of the status bar.




## -see-also




<a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>
 

 

