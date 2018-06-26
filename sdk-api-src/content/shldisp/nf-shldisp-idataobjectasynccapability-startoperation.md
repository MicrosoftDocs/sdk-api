---
UID: NF:shldisp.IDataObjectAsyncCapability.StartOperation
title: IDataObjectAsyncCapability::StartOperation
author: windows-sdk-content
description: Called by a drop target to indicate that asynchronous data extraction is starting.
old-location: shell\IDataObjectAsyncCapability_StartOperation.htm
old-project: shell
ms.assetid: 84C1E709-ADFD-4c00-B767-C0DB4C30578A
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IDataObjectAsyncCapability interface [Windows Shell],StartOperation method, IDataObjectAsyncCapability.StartOperation, IDataObjectAsyncCapability::StartOperation, StartOperation, StartOperation method [Windows Shell], StartOperation method [Windows Shell],IDataObjectAsyncCapability interface, shell.IDataObjectAsyncCapability_StartOperation, shldisp/IDataObjectAsyncCapability::StartOperation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDataObjectAsyncCapability.StartOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IDataObjectAsyncCapability::StartOperation


## -description


Called by a drop target to indicate that asynchronous data extraction is starting.


## -parameters




### -param pbcReserved [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

Reserved. Set this value to <b>nullptr</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The drop target calls this method to notify the data object that asynchronous data extraction is starting. The method should store this information so that it can be returned by <a href="https://msdn.microsoft.com/858EB8C4-88AB-40a3-B4FC-CCD19235CE55">IDataObjectAsyncCapability::InOperation</a>. Once <b>StartOperation</b> has been called, the drop target returns the <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a> call as it would for normal synchronous data extraction.




## -see-also




<a href="https://msdn.microsoft.com/2E23A137-0C5B-4ce9-8100-758C7E17753B">IDataObjectAsyncCapability</a>
 

 

