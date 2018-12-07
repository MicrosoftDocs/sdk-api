---
UID: NF:shobjidl.ICommDlgBrowser3.OnPreViewCreated
title: ICommDlgBrowser3::OnPreViewCreated
author: windows-sdk-content
description: Called after a specified preview is created in the IShellView interface.
old-location: shell\ICommDlgBrowser3_OnPreViewCreated.htm
tech.root: shell
ms.assetid: 1506f553-e0b0-4d6b-9d63-15f3a2d38112
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICommDlgBrowser3 interface [Windows Shell],OnPreViewCreated method, ICommDlgBrowser3.OnPreViewCreated, ICommDlgBrowser3::OnPreViewCreated, OnPreViewCreated, OnPreViewCreated method [Windows Shell], OnPreViewCreated method [Windows Shell],ICommDlgBrowser3 interface, _shell_ICommDlgBrowser3_OnPreViewCreated, shell.ICommDlgBrowser3_OnPreViewCreated, shobjidl/ICommDlgBrowser3::OnPreViewCreated
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
 - ICommDlgBrowser3.OnPreViewCreated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICommDlgBrowser3::OnPreViewCreated


## -description


Called after a specified preview is created in the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.


## -parameters




### -param ppshv [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface of the hosted view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



