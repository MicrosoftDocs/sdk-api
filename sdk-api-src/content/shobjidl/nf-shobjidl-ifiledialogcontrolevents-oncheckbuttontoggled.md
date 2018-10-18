---
UID: NF:shobjidl.IFileDialogControlEvents.OnCheckButtonToggled
title: IFileDialogControlEvents::OnCheckButtonToggled
author: windows-sdk-content
description: Called when the user changes the state of a check button (check box).
old-location: shell\IFileDialogControlEvents_OnCheckButtonToggled.htm
tech.root: shell
ms.assetid: 97e6cb2a-1ffc-43ca-abb6-f1b259e8fcd2
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IFileDialogControlEvents interface [Windows Shell],OnCheckButtonToggled method, IFileDialogControlEvents.OnCheckButtonToggled, IFileDialogControlEvents::OnCheckButtonToggled, OnCheckButtonToggled, OnCheckButtonToggled method [Windows Shell], OnCheckButtonToggled method [Windows Shell],IFileDialogControlEvents interface, shell.IFileDialogControlEvents_OnCheckButtonToggled, shell_IFileDialogControlEvents_OnCheckButtonToggled, shobjidl/IFileDialogControlEvents::OnCheckButtonToggled
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IFileDialogControlEvents.OnCheckButtonToggled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogControlEvents::OnCheckButtonToggled


## -description


Called when the user changes the state of a check button (check box).


## -parameters




### -param pfdc [in]

Type: <b><a href="https://msdn.microsoft.com/f1c29688-3538-40ff-a1da-6211cc5dded7">IFileDialogCustomize</a>*</b>

A pointer to the interface through which the application added controls to the dialog.


### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the button that the user clicked.


### -param bChecked [in]

Type: <b>BOOL</b>

A <b>BOOL</b> indicating the current state of the check button. <b>TRUE</b> if checked; <b>FALSE</b> otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



