---
UID: NF:shobjidl_core.IFileDialog.GetResult
title: IFileDialog::GetResult
author: windows-sdk-content
description: Gets the choice that the user made in the dialog.
old-location: shell\IFileDialog_GetResult.htm
tech.root: shell
ms.assetid: 6572f172-8b66-4b42-b087-d0133595b380
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetResult, GetResult method [Windows Shell], GetResult method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetResult method, IFileDialog.GetResult, IFileDialog::GetResult, shell.IFileDialog_GetResult, shell_IFileDialog_GetResult, shobjidl_core/IFileDialog::GetResult
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
 - IFileDialog.GetResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::GetResult


## -description


Gets the choice that the user made in the dialog.


## -parameters




### -param ppsi [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the user's choice.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IFileDialog::GetResult</b> can be called after the dialog has closed or during the handling of an <a href="https://msdn.microsoft.com/81277122-b2fe-40af-85f8-d578925856a1">OnFileOk</a> event. Calling this method at any other time will fail. If multiple items were chosen, this method will fail. In the case of multiple items, call <a href="https://msdn.microsoft.com/5c710dae-4988-4f19-beb5-2ff9cd11c596">GetResults</a>



<a href="https://msdn.microsoft.com/0284b694-64d1-48db-bef3-92f808b29b23">Show</a> must return a success code for a result to be available to <b>IFileDialog::GetResult</b>.




## -see-also




<a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>



<a href="https://msdn.microsoft.com/b3768c15-d933-43c0-8398-f8f1c16ecbf9">IFileDialog::GetCurrentSelection</a>
 

 

