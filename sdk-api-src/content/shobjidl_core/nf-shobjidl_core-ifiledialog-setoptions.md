---
UID: NF:shobjidl_core.IFileDialog.SetOptions
title: IFileDialog::SetOptions
author: windows-sdk-content
description: Sets flags to control the behavior of the dialog.
old-location: shell\IFileDialog_SetOptions.htm
old-project: shell
ms.assetid: 99def5c2-3fc3-416c-80a6-6009927ab63e
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IFileDialog interface [Windows Shell],SetOptions method, IFileDialog.SetOptions, IFileDialog::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetOptions, shell_IFileDialog_SetOptions, shobjidl_core/IFileDialog::SetOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IFileDialog.SetOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::SetOptions


## -description


Sets flags to control the behavior of the dialog.


## -parameters




### -param fos [in]

Type: <b>FILEOPENDIALOGOPTIONS</b>

One or more of the <a href="https://msdn.microsoft.com/CDDB4B39-AFB9-4C0D-9D5A-0F2EA9EABE64">FILEOPENDIALOGOPTIONS</a> values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Generally, this method should take the value that was retrieved by <a href="https://msdn.microsoft.com/8a01b64d-b58e-4470-a5ed-8cf821b26c6b">IFileDialog::GetOptions</a> and modify it to include or exclude options by setting the appropriate flags.



