---
UID: NF:shobjidl_core.IFileDialog.GetFileTypeIndex
title: IFileDialog::GetFileTypeIndex
author: windows-sdk-content
description: Gets the currently selected file type.
old-location: shell\IFileDialog_GetFileTypeIndex.htm
old-project: shell
ms.assetid: ae5b08a1-a97d-433b-88dc-938abe028384
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetFileTypeIndex, GetFileTypeIndex method [Windows Shell], GetFileTypeIndex method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetFileTypeIndex method, IFileDialog.GetFileTypeIndex, IFileDialog::GetFileTypeIndex, shell.IFileDialog_GetFileTypeIndex, shell_IFileDialog_GetFileTypeIndex, shobjidl_core/IFileDialog::GetFileTypeIndex
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
 - IFileDialog.GetFileTypeIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::GetFileTypeIndex


## -description


Gets the currently selected file type.


## -parameters




### -param piFileType [out]

Type: <b>UINT*</b>

A pointer to a <b>UINT</b> value that receives the index of the selected file type in the file type array passed to <a href="https://msdn.microsoft.com/ca850988-7f2f-4faf-9ded-14db476fc452">IFileDialog::SetFileTypes</a> in its <i>cFileTypes</i> parameter.

<div class="alert"><b>Note</b>  This is a one-based index rather than zero-based.</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IFileDialog::GetFileTypeIndex</b> can be called either while the dialog is open or after it has closed.



