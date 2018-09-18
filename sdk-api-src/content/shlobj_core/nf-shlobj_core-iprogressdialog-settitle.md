---
UID: NF:shlobj_core.IProgressDialog.SetTitle
title: IProgressDialog::SetTitle
author: windows-sdk-content
description: Sets the title of the progress dialog box.
old-location: shell\IProgressDialog_SetTitle.htm
tech.root: shell
ms.assetid: c5474ab2-bd13-45ba-9df5-977b909b0726
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetTitle method, IProgressDialog.SetTitle, IProgressDialog::SetTitle, SetTitle, SetTitle method [Windows Shell], SetTitle method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetTitle, shell.IProgressDialog_SetTitle, shlobj_core/IProgressDialog::SetTitle
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
 - IProgressDialog.SetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressDialog::SetTitle


## -description


Sets the title of the progress dialog box.


## -parameters




### -param pwzTitle [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that contains the dialog box title.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ba0fb1f9-f67f-4cc7-96d8-4c4ccdd213eb">IProgressDialog</a>
 

 

