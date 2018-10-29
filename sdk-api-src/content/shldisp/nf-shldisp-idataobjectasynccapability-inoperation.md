---
UID: NF:shldisp.IDataObjectAsyncCapability.InOperation
title: IDataObjectAsyncCapability::InOperation
author: windows-sdk-content
description: Called by the drop source to determine whether the target is extracting data asynchronously.
old-location: shell\IDataObjectAsyncCapability_InOperation.htm
tech.root: shell
ms.assetid: 858EB8C4-88AB-40a3-B4FC-CCD19235CE55
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDataObjectAsyncCapability interface [Windows Shell],InOperation method, IDataObjectAsyncCapability.InOperation, IDataObjectAsyncCapability::InOperation, InOperation, InOperation method [Windows Shell], InOperation method [Windows Shell],IDataObjectAsyncCapability interface, shell.IDataObjectAsyncCapability_InOperation, shldisp/IDataObjectAsyncCapability::InOperation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDataObjectAsyncCapability.InOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataObjectAsyncCapability::InOperation


## -description


Called by the drop source to determine whether the target is extracting data asynchronously.


## -parameters




### -param pfInAsyncOp [out]

Type: <b>BOOL*</b>

<b>VARIANT_TRUE</b> if data extraction is being handled asynchronously; otherwise, <b>VARIANT_FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by the drop source after <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> returns. The <i>pfInAsyncOp</i> parameter should be set to <b>VARIANT_TRUE</b> only if the drop target has called <a href="https://msdn.microsoft.com/84C1E709-ADFD-4c00-B767-C0DB4C30578A">IDataObjectAsyncCapability::StartOperation</a>.




## -see-also




<a href="https://msdn.microsoft.com/2E23A137-0C5B-4ce9-8100-758C7E17753B">IDataObjectAsyncCapability</a>
 

 

