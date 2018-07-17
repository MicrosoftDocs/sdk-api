---
UID: NF:shobjidl_core.IFileDialogCustomize.EnableOpenDropDown
title: IFileDialogCustomize::EnableOpenDropDown
author: windows-sdk-content
description: Enables a drop-down list on the Open or Save button in the dialog.
old-location: shell\IFileDialogCustomize_EnableOpenDropDown.htm
old-project: shell
ms.assetid: b4626030-0fc7-4329-b897-01f4ce8728a0
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: EnableOpenDropDown, EnableOpenDropDown method [Windows Shell], EnableOpenDropDown method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],EnableOpenDropDown method, IFileDialogCustomize.EnableOpenDropDown, IFileDialogCustomize::EnableOpenDropDown, shell.IFileDialogCustomize_EnableOpenDropDown, shell_IFileDialogCustomize_EnableOpenDropDown, shobjidl_core/IFileDialogCustomize::EnableOpenDropDown
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
 - IFileDialogCustomize.EnableOpenDropDown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::EnableOpenDropDown


## -description


Enables a drop-down list on the <b>Open</b> or <b>Save</b> button in the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the drop-down list.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Open or Save button label takes on the text of the first item in the drop-down. This overrides any label set by <a href="https://msdn.microsoft.com/4320de0f-bfa6-4e17-a09d-d004559fae70">IFileDialog::SetOkButtonLabel</a>.

 Use <a href="https://msdn.microsoft.com/56d7d0df-0c3e-4bc3-b91e-3b191f5dad76">IFileDialogCustomize::AddControlItem</a> to add items to the drop-down.



