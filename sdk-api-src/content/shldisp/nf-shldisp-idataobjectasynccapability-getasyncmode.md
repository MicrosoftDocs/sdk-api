---
UID: NF:shldisp.IDataObjectAsyncCapability.GetAsyncMode
title: IDataObjectAsyncCapability::GetAsyncMode
author: windows-sdk-content
description: Called by a drop target to determine whether the data object supports asynchronous data extraction.
old-location: shell\IDataObjectAsyncCapability_GetAsyncMode.htm
tech.root: shell
ms.assetid: 0B7A4299-4D19-4c5a-99A5-9568F4D58061
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetAsyncMode, GetAsyncMode method [Windows Shell], GetAsyncMode method [Windows Shell],IDataObjectAsyncCapability interface, IDataObjectAsyncCapability interface [Windows Shell],GetAsyncMode method, IDataObjectAsyncCapability.GetAsyncMode, IDataObjectAsyncCapability::GetAsyncMode, shell.IDataObjectAsyncCapability_GetAsyncMode, shldisp/IDataObjectAsyncCapability::GetAsyncMode
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
 - IDataObjectAsyncCapability.GetAsyncMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

