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

# IDataObjectAsyncCapability::SetAsyncMode


## -description


Called by a drop source to specify whether the data object supports asynchronous data extraction.


## -parameters




### -param fDoOpAsync [in]

Type: <b>BOOL</b>

<b>VARIANT_TRUE</b> if an asynchronous operation is supported; otherwise, <b>VARIANT_FALSE</b>. The default value is <b>VARIANT_FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by the drop source to indicate that the data object supports asynchronous data extraction. Store the <i>fDoOpAsync</i> for later use by <a href="https://msdn.microsoft.com/0B7A4299-4D19-4c5a-99A5-9568F4D58061">IDataObjectAsyncCapability::GetAsyncMode</a>. The drop target determines whether asynchronous data extraction is supported by calling <b>IDataObjectAsyncCapability::GetAsyncMode</b> to retrieve the <i>fDoOpAsync</i> value.

If <i>fDoOpAsync</i> is set to <b>VARIANT_TRUE</b>, <b>SetAsyncMode</b> must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IDataObjectAsyncCapability::AddRef</a>, and store the interface pointer for use by <a href="https://msdn.microsoft.com/CF9D2A95-12AF-4538-882D-B391F2E087ED">IDataObjectAsyncCapability::EndOperation</a>.




## -see-also




<a href="https://msdn.microsoft.com/2E23A137-0C5B-4ce9-8100-758C7E17753B">IDataObjectAsyncCapability</a>
 

 

