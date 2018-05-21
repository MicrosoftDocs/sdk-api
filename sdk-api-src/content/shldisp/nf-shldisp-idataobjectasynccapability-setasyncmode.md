---
UID: NF:shldisp.IDataObjectAsyncCapability.SetAsyncMode
title: IDataObjectAsyncCapability::SetAsyncMode
author: windows-driver-content
description: Called by a drop source to specify whether the data object supports asynchronous data extraction.
old-location: shell\IDataObjectAsyncCapability_SetAsyncMode.htm
old-project: shell
ms.assetid: 97DCCA78-F25E-47de-8292-F0C6ED9DFD35
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDataObjectAsyncCapability interface [Windows Shell],SetAsyncMode method, IDataObjectAsyncCapability.SetAsyncMode, IDataObjectAsyncCapability::SetAsyncMode, SetAsyncMode, SetAsyncMode method [Windows Shell], SetAsyncMode method [Windows Shell],IDataObjectAsyncCapability interface, shell.IDataObjectAsyncCapability_SetAsyncMode, shldisp/IDataObjectAsyncCapability::SetAsyncMode
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IDataObjectAsyncCapability.SetAsyncMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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
 

 

