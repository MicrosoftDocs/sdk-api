---
UID: NF:shlobj_core.IProgressDialog.SetCancelMsg
title: IProgressDialog::SetCancelMsg
author: windows-sdk-content
description: Sets a message to be displayed if the user cancels the operation.
old-location: shell\IProgressDialog_SetCancelMsg.htm
tech.root: shell
ms.assetid: 520e11c0-f356-45e1-a300-cc14e88eb42e
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetCancelMsg method, IProgressDialog.SetCancelMsg, IProgressDialog::SetCancelMsg, SetCancelMsg, SetCancelMsg method [Windows Shell], SetCancelMsg method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetCancelMsg, shell.IProgressDialog_SetCancelMsg, shlobj_core/IProgressDialog::SetCancelMsg
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IProgressDialog.SetCancelMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressDialog::SetCancelMsg


## -description


Sets a message to be displayed if the user cancels the operation.


## -parameters




### -param pwzCancelMsg [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that contains the message to be displayed.


### -param pvResevered

TBD




#### - pvReserved

Type: <b>LPCVOID</b>

Reserved. Set to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Even though the user clicks <b>Cancel</b>, the application cannot immediately call <a href="https://msdn.microsoft.com/6a46ca72-b19d-4fd3-b783-2d182326deb4">IProgressDialog::StopProgressDialog</a> to close the dialog box. The application must wait until the next time it calls <a href="https://msdn.microsoft.com/bd817850-7776-47cd-b1b3-ccb946660781">IProgressDialog::HasUserCancelled</a> to discover that the user has canceled the operation. Since this delay might be significant, the progress dialog box provides the user with immediate feedback by clearing text lines 1 and 2 and displaying the cancel message on line 3. The message is intended to let the user know that the delay is normal and that the progress dialog box will be closed shortly. It is typically is set to something like "Please wait while ...".




## -see-also




<a href="https://msdn.microsoft.com/ba0fb1f9-f67f-4cc7-96d8-4c4ccdd213eb">IProgressDialog</a>
 

 

