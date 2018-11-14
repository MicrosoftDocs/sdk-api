---
UID: NF:shobjidl_core.ICommDlgBrowser.OnDefaultCommand
title: ICommDlgBrowser::OnDefaultCommand
author: windows-sdk-content
description: Called when a user double-clicks in the view or presses the ENTER key.
old-location: shell\ICommDlgBrowser_OnDefaultCommand.htm
tech.root: shell
ms.assetid: 827af758-63df-42bb-9ecf-087bc974710a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICommDlgBrowser interface [Windows Shell],OnDefaultCommand method, ICommDlgBrowser.OnDefaultCommand, ICommDlgBrowser::OnDefaultCommand, OnDefaultCommand, OnDefaultCommand method [Windows Shell], OnDefaultCommand method [Windows Shell],ICommDlgBrowser interface, _win32_ICommDlgBrowser_OnDefaultCommand, shell.ICommDlgBrowser_OnDefaultCommand, shobjidl_core/ICommDlgBrowser::OnDefaultCommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - ICommDlgBrowser.OnDefaultCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- ICommDlgBrowser.OnDefaultCommand
: 
---

# ICommDlgBrowser::OnDefaultCommand


## -description


Called when a user double-clicks in the view or presses the ENTER key.


## -parameters




### -param ppshv

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the view's <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The browser should return S_OK if it has processed the action or S_FALSE to let the view perform the default action.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
This method allows the default command to be handled by the common dialog box instead of the view.




## -see-also




<a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a>
 

 

