---
UID: NF:shobjidl_core.IFileDialog.GetFileName
title: IFileDialog::GetFileName
author: windows-sdk-content
description: Retrieves the text currently entered in the dialog's File name edit box.
old-location: shell\IFileDialog_GetFileName.htm
old-project: shell
ms.assetid: d27acb22-906a-4e5e-9239-6de3162fd263
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetFileName, GetFileName method [Windows Shell], GetFileName method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetFileName method, IFileDialog.GetFileName, IFileDialog::GetFileName, shell.IFileDialog_GetFileName, shell_IFileDialog_GetFileName, shobjidl_core/IFileDialog::GetFileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IFileDialog.GetFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::GetFileName


## -description


Retrieves the text currently entered in the dialog's <b>File name</b> edit box.


## -parameters




### -param pszName [out]

Type: <b>WCHAR**</b>

The address of a pointer to a buffer that, when this method returns successfully, receives the text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The text in the <b>File name</b> edit box does not necessarily reflect the item the user chose.  To get the item the user chose, use <a href="https://msdn.microsoft.com/6572f172-8b66-4b42-b087-d0133595b380">IFileDialog::GetResult</a>.

The calling application is responsible for releasing the retrieved buffer by using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.



