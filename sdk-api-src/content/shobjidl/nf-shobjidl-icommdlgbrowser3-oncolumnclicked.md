---
UID: NF:shobjidl.ICommDlgBrowser3.OnColumnClicked
title: ICommDlgBrowser3::OnColumnClicked
author: windows-sdk-content
description: Called after a specified column is clicked in the IShellView interface.
old-location: shell\ICommDlgBrowser3_OnColumnClicked.htm
tech.root: shell
ms.assetid: 19cd3dc6-14e4-494d-b4d7-2c9d4fd0fe55
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ICommDlgBrowser3 interface [Windows Shell],OnColumnClicked method, ICommDlgBrowser3.OnColumnClicked, ICommDlgBrowser3::OnColumnClicked, OnColumnClicked, OnColumnClicked method [Windows Shell], OnColumnClicked method [Windows Shell],ICommDlgBrowser3 interface, _shell_ICommDlgBrowser3_OnColumnClicked, shell.ICommDlgBrowser3_OnColumnClicked, shobjidl/ICommDlgBrowser3::OnColumnClicked
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
 - ICommDlgBrowser3.OnColumnClicked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICommDlgBrowser3::OnColumnClicked


## -description


Called after a specified column is clicked in the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.


## -parameters




### -param ppshv [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface of the hosted view.


### -param iColumn [in]

Type: <b>int</b>

The index of the column clicked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



