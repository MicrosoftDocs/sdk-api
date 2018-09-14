---
UID: NF:shobjidl_core.IFileDialog.Close
title: IFileDialog::Close
author: windows-sdk-content
description: Closes the dialog.
old-location: shell\IFileDialog_Close.htm
tech.root: shell
ms.assetid: 064b035a-c554-4c81-93b9-ba4fb92da09d
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: Close, Close method [Windows Shell], Close method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],Close method, IFileDialog.Close, IFileDialog::Close, shell.IFileDialog_Close, shell_IFileDialog_Close, shobjidl_core/IFileDialog::Close
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
 - IFileDialog.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::Close


## -description


Closes the dialog.


## -parameters




### -param hr [in]

Type: <b>HRESULT</b>

The code that will be returned by <a href="https://msdn.microsoft.com/0284b694-64d1-48db-bef3-92f808b29b23">Show</a> to indicate that the dialog was closed before a selection was made.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application can call this method from a callback method or function while the dialog is open. The dialog will close and the <a href="https://msdn.microsoft.com/0284b694-64d1-48db-bef3-92f808b29b23">Show</a> method will return with the <b>HRESULT</b> specified in <i>hr</i>.

If this method is called, there is no result available for the <a href="https://msdn.microsoft.com/6572f172-8b66-4b42-b087-d0133595b380">IFileDialog::GetResult</a> or <a href="https://msdn.microsoft.com/5c710dae-4988-4f19-beb5-2ff9cd11c596">GetResults</a> methods, and they will fail if called.



