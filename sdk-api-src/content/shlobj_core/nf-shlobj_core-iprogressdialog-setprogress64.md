---
UID: NF:shlobj_core.IProgressDialog.SetProgress64
title: IProgressDialog::SetProgress64
author: windows-sdk-content
description: Updates the progress dialog box with the current state of the operation.
old-location: shell\IProgressDialog_SetProgress64.htm
old-project: shell
ms.assetid: 829775a0-5dd0-4c5e-8b92-b34c7d75f15e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetProgress64 method, IProgressDialog.SetProgress64, IProgressDialog::SetProgress64, SetProgress64, SetProgress64 method [Windows Shell], SetProgress64 method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetProgress64, shell.IProgressDialog_SetProgress64, shlobj_core/IProgressDialog::SetProgress64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IProgressDialog.SetProgress64
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IProgressDialog::SetProgress64


## -description


Updates the progress dialog box with the current state of the operation.


## -parameters




### -param ullCompleted [in]

Type: <b>ULONGLONG</b>

An application-defined value that indicates what proportion of the operation has been completed at the time the method was called.


### -param ullTotal [in]

Type: <b>ULONGLONG</b>

An application-defined value that specifies what value <i>ullCompleted</i> will have when the operation is complete.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method has exactly the same function as <a href="https://msdn.microsoft.com/50df7b32-e345-4379-809f-6870b53417b8">IProgressDialog::SetProgress</a> but allows you to use values larger than one <b>DWORD</b> (4 GB).




## -see-also




<a href="https://msdn.microsoft.com/ba0fb1f9-f67f-4cc7-96d8-4c4ccdd213eb">IProgressDialog</a>
 

 

