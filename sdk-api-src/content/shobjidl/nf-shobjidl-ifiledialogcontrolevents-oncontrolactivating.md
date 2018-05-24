---
UID: NF:shobjidl.IFileDialogControlEvents.OnControlActivating
title: IFileDialogControlEvents::OnControlActivating
author: windows-driver-content
description: Called when an Open button drop-down list customized through EnableOpenDropDown or a Tools menu is about to display its contents.
old-location: shell\IFileDialogControlEvents_OnControlActivating.htm
old-project: shell
ms.assetid: 12efb183-65b9-4095-be57-7c7802bda2ce
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IFileDialogControlEvents interface [Windows Shell],OnControlActivating method, IFileDialogControlEvents.OnControlActivating, IFileDialogControlEvents::OnControlActivating, OnControlActivating, OnControlActivating method [Windows Shell], OnControlActivating method [Windows Shell],IFileDialogControlEvents interface, shell.IFileDialogControlEvents_OnControlActivating, shell_IFileDialogControlEvents_OnControlActivating, shobjidl/IFileDialogControlEvents::OnControlActivating
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	IFileDialogControlEvents.OnControlActivating
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IFileDialogControlEvents::OnControlActivating


## -description


Called when an <b>Open</b> button drop-down list customized through <a href="https://msdn.microsoft.com/b4626030-0fc7-4329-b897-01f4ce8728a0">EnableOpenDropDown</a> or a <b>Tools</b> menu is about to display its contents.


## -parameters




### -param pfdc [in]

Type: <b><a href="https://msdn.microsoft.com/f1c29688-3538-40ff-a1da-6211cc5dded7">IFileDialogCustomize</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/f1c29688-3538-40ff-a1da-6211cc5dded7">IFileDialogCustomize</a> object through which the application adds controls to the dialog.


### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the list or menu about to display.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In response to this notification, an application can update the contents of the menu or list about to be displayed, based on the current state of the dialog.



