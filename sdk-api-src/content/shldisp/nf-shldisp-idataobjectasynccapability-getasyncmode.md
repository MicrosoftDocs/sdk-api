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

# IDataObjectAsyncCapability::GetAsyncMode


## -description


Called by a drop target to determine whether the data object supports asynchronous data extraction.


## -parameters




### -param pfIsOpAsync [out]

Type: <b>BOOL*</b>

<b>VARIANT_TRUE</b> if an asynchronous operation is supported; otherwise, <b>VARIANT_FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The purpose of this method is to give the drop target the value of the <a href="https://msdn.microsoft.com/97DCCA78-F25E-47de-8292-F0C6ED9DFD35">IDataObjectAsyncCapability::SetAsyncMode</a> method's <i>fDoOpAsync</i> parameter. This parameter is set to <b>VARIANT_FALSE</b> by default. If the data object supports asynchronous data extraction, it must call <b>IDataObjectAsyncCapability::SetAsyncMode</b> and set <i>fDoOpAsync</i> to <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/2E23A137-0C5B-4ce9-8100-758C7E17753B">IDataObjectAsyncCapability</a>
 

 

