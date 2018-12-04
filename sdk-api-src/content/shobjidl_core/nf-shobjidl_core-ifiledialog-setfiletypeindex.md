---
UID: NF:shobjidl_core.IFileDialog.SetFileTypeIndex
title: IFileDialog::SetFileTypeIndex
author: windows-sdk-content
description: Sets the file type that appears as selected in the dialog.
old-location: shell\IFileDialog_SetFileTypeIndex.htm
tech.root: shell
ms.assetid: 733ade05-e255-4b1c-a961-e1feb749f73d
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFileTypeIndex method, IFileDialog.SetFileTypeIndex, IFileDialog::SetFileTypeIndex, SetFileTypeIndex, SetFileTypeIndex method [Windows Shell], SetFileTypeIndex method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetFileTypeIndex, shell_IFileDialog_SetFileTypeIndex, shobjidl_core/IFileDialog::SetFileTypeIndex
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
 - IFileDialog.SetFileTypeIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::SetFileTypeIndex


## -description


Sets the file type that appears as selected in the dialog.


## -parameters




### -param iFileType [in]

Type: <b>UINT</b>

The index of the file type in the file type array passed to <a href="https://msdn.microsoft.com/ca850988-7f2f-4faf-9ded-14db476fc452">IFileDialog::SetFileTypes</a> in its <i>cFileTypes</i> parameter. Note that this is a one-based index, not zero-based.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method must be called before the dialog is showing.



