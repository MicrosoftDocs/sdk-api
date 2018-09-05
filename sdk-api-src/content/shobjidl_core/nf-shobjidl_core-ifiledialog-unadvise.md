---
UID: NF:shobjidl_core.IFileDialog.Unadvise
title: IFileDialog::Unadvise
author: windows-sdk-content
description: Removes an event handler that was attached through the IFileDialog::Advise method.
old-location: shell\IFileDialog_Unadvise.htm
old-project: shell
ms.assetid: 48504141-6612-43fe-8470-a9871b560f1a
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IFileDialog interface [Windows Shell],Unadvise method, IFileDialog.Unadvise, IFileDialog::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IFileDialog interface, shell.IFileDialog_Unadvise, shell_IFileDialog_Unadvise, shobjidl_core/IFileDialog::Unadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialog.Unadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::Unadvise


## -description


Removes an event handler that was attached through the <a href="https://msdn.microsoft.com/f5664a52-f26c-475d-84ef-0c657ae46e2e">IFileDialog::Advise</a> method.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

The <b>DWORD</b> value that represents the event handler. This value is obtained through the <i>pdwCookie</i> parameter of the <a href="https://msdn.microsoft.com/f5664a52-f26c-475d-84ef-0c657ae46e2e">IFileDialog::Advise</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



