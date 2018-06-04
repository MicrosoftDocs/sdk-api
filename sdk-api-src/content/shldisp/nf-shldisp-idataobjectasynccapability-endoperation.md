---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDataObjectAsyncCapability::EndOperation


## -description


Notifies the data object that the asynchronous data extraction has ended.


## -parameters




### -param hResult [in]

Type: <b>HRESULT</b>

Indicates the outcome of the data extraction. Set this value to S_OK if successful, or a COM error code otherwise.


### -param pbcReserved [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

Reserved. Set to <b>nullptr</b>.


### -param dwEffects [in]

Type: <b>DWORD</b>

A <a href="https://msdn.microsoft.com/d8e46899-3fbf-4012-8dd3-67fa627526d5">DROPEFFECT</a> value that indicates the result of an optimized move. This should be the same value that would be passed to the data object as a CFSTR_PERFORMEDDROPEFFECT format with a normal data extraction operation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>EndOperation</b> retrieves the <a href="https://msdn.microsoft.com/2E23A137-0C5B-4ce9-8100-758C7E17753B">IDataObjectAsyncCapability</a> pointer stored by <a href="https://msdn.microsoft.com/97DCCA78-F25E-47de-8292-F0C6ED9DFD35">IDataObjectAsyncCapability::SetAsyncMode</a> and passes its parameter values to that interface's <b>IDataObjectAsyncCapability::EndOperation</b> method. <b>EndOperation</b> then releases the <b>IDataObjectAsyncCapability</b> pointer.

<b>EndOperation</b> is also responsible for any associated clean-up operations. When finished, <b>EndOperation</b> should notify the drop source through a private interface.




## -see-also




<a href="https://msdn.microsoft.com/2E23A137-0C5B-4ce9-8100-758C7E17753B">IDataObjectAsyncCapability</a>
 

 

