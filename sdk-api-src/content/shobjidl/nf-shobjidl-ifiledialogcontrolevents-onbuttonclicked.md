---
UID: NF:shobjidl.IFileDialogControlEvents.OnButtonClicked
title: IFileDialogControlEvents::OnButtonClicked
author: windows-sdk-content
description: Called when the user clicks a command button.
old-location: shell\IFileDialogControlEvents_OnButtonClicked.htm
tech.root: shell
ms.assetid: 46dc28a4-717f-42b6-bff7-56f4902f075c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileDialogControlEvents interface [Windows Shell],OnButtonClicked method, IFileDialogControlEvents.OnButtonClicked, IFileDialogControlEvents::OnButtonClicked, OnButtonClicked, OnButtonClicked method [Windows Shell], OnButtonClicked method [Windows Shell],IFileDialogControlEvents interface, shell.IFileDialogControlEvents_OnButtonClicked, shell_IFileDialogControlEvents_OnButtonClicked, shobjidl/IFileDialogControlEvents::OnButtonClicked
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
 - IFileDialogControlEvents.OnButtonClicked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogControlEvents::OnButtonClicked


## -description


Called when the user clicks a command button.


## -parameters




### -param pfdc [in]

Type: <b><a href="https://msdn.microsoft.com/f1c29688-3538-40ff-a1da-6211cc5dded7">IFileDialogCustomize</a>*</b>

A pointer to the interface through which the application added controls to the dialog.


### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the button that the user clicked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



