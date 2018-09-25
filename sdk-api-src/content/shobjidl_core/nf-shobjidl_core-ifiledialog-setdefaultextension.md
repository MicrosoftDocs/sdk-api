---
UID: NF:shobjidl_core.IFileDialog.SetDefaultExtension
title: IFileDialog::SetDefaultExtension
author: windows-sdk-content
description: Sets the default extension to be added to file names.
old-location: shell\IFileDialog_SetDefaultExtension.htm
tech.root: shell
ms.assetid: 2e1739f4-d229-4bf1-99f4-6bded830de2b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IFileDialog interface [Windows Shell],SetDefaultExtension method, IFileDialog.SetDefaultExtension, IFileDialog::SetDefaultExtension, SetDefaultExtension, SetDefaultExtension method [Windows Shell], SetDefaultExtension method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetDefaultExtension, shell_IFileDialog_SetDefaultExtension, shobjidl_core/IFileDialog::SetDefaultExtension
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialog.SetDefaultExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::SetDefaultExtension


## -description


Sets the default extension to be added to file names.


## -parameters




### -param pszDefaultExtension [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the extension text. This string should not include a leading period. For example, "jpg" is correct, while ".jpg" is not.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method is called before showing the dialog, the dialog will update the default extension automatically when the user chooses a new file type (see <a href="https://msdn.microsoft.com/ca850988-7f2f-4faf-9ded-14db476fc452">SetFileTypes</a>).



