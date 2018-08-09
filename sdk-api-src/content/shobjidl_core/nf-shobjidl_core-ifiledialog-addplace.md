---
UID: NF:shobjidl_core.IFileDialog.AddPlace
title: IFileDialog::AddPlace
author: windows-sdk-content
description: Adds a folder to the list of places available for the user to open or save items.
old-location: shell\IFileDialog_AddPlace.htm
old-project: shell
ms.assetid: 2196e73f-4e0f-4213-b0a2-13a047486f40
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddPlace, AddPlace method [Windows Shell], AddPlace method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],AddPlace method, IFileDialog.AddPlace, IFileDialog::AddPlace, shell.IFileDialog_AddPlace, shell_IFileDialog_AddPlace, shobjidl_core/IFileDialog::AddPlace
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
 - IFileDialog.AddPlace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::AddPlace


## -description


Adds a folder to the list of places available for the user to open or save items.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the folder to be made available to the user. This can only be a folder.


### -param fdap [in]

Type: <b><a href="https://msdn.microsoft.com/96865947-abd1-4045-9bb2-5839e9592ad2">FDAP</a></b>

Specifies where the folder is placed within the list. See <a href="https://msdn.microsoft.com/96865947-abd1-4045-9bb2-5839e9592ad2">FDAP</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/779b1b2e-cd4b-404f-9d50-ac87b81640d2">SHSetTemporaryPropertyForItem</a> can be used to set a temporary <a href="https://msdn.microsoft.com/fdb6b0fa-0741-4edc-8902-763a461313b9">PKEY_ItemNameDisplay</a> property on the item represented by the <i>psi</i> parameter. The value for this property will be used in place of the item's UI name.



