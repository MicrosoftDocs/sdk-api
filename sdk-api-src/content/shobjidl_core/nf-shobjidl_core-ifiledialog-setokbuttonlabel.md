---
UID: NF:shobjidl_core.IFileDialog.SetOkButtonLabel
title: IFileDialog::SetOkButtonLabel
author: windows-sdk-content
description: Sets the text of the Open or Save button.
old-location: shell\IFileDialog_SetOkButtonLabel.htm
tech.root: shell
ms.assetid: 4320de0f-bfa6-4e17-a09d-d004559fae70
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFileDialog interface [Windows Shell],SetOkButtonLabel method, IFileDialog.SetOkButtonLabel, IFileDialog::SetOkButtonLabel, SetOkButtonLabel, SetOkButtonLabel method [Windows Shell], SetOkButtonLabel method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetOkButtonLabel, shell_IFileDialog_SetOkButtonLabel, shobjidl_core/IFileDialog::SetOkButtonLabel
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
 - IFileDialog.SetOkButtonLabel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::SetOkButtonLabel


## -description


Sets the text of the <b>Open</b> or <b>Save</b> button.


## -parameters




### -param pszText [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the button text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



