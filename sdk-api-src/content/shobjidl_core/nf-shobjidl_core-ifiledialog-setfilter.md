---
UID: NF:shobjidl_core.IFileDialog.SetFilter
title: IFileDialog::SetFilter
author: windows-sdk-content
description: SetFilter is no longer available for use as of Windows 7.
old-location: shell\IFileDialog_SetFilter.htm
tech.root: shell
ms.assetid: 6f650ae2-77c4-496c-8b8b-279c69eaaf65
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFilter method, IFileDialog.SetFilter, IFileDialog::SetFilter, SetFilter, SetFilter method [Windows Shell], SetFilter method [Windows Shell],IFileDialog interface, _shell_IFileDialog_SetFilter, shell.IFileDialog_SetFilter, shobjidl_core/IFileDialog::SetFilter
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
 - IFileDialog.SetFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::SetFilter


## -description


<p class="CCE_Message">[Deprecated. <b>SetFilter</b> is no longer available for use as of Windows 7.]

Sets the filter.


## -parameters




### -param pFilter

Type: <b><a href="https://msdn.microsoft.com/c2873385-a25d-4d9d-94ef-05dcdf284be1">IShellItemFilter</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/c2873385-a25d-4d9d-94ef-05dcdf284be1">IShellItemFilter</a> that is to be set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be used if the application needs to perform special filtering to remove some items from the dialog box's view.  <a href="https://msdn.microsoft.com/39ec171e-24a0-40ff-b199-36b5a2809164">IncludeItem</a> will be called for each item that would normally be included in the view. <a href="https://msdn.microsoft.com/a84868ab-25c4-4cb7-84a1-aba0eff09b4a">GetEnumFlagsForItem</a> is not used.
To filter by file type, <a href="https://msdn.microsoft.com/ca850988-7f2f-4faf-9ded-14db476fc452">IFileDialog::SetFileTypes</a> should be used, because in folders with a large number of items it may offer better performance than applying an <a href="https://msdn.microsoft.com/c2873385-a25d-4d9d-94ef-05dcdf284be1">IShellItemFilter</a>.




