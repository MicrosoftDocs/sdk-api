---
UID: NF:qnetwork.IAMNetShowExProps.get_ErrorCorrection
title: IAMNetShowExProps::get_ErrorCorrection
author: windows-sdk-content
description: The get_ErrorCorrection method retrieves the current error correction method.
old-location: dshow\iamnetshowexprops_get_errorcorrection.htm
tech.root: DirectShow
ms.assetid: ab731d68-969b-425d-978a-879b15c06a88
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMNetShowExProps interface [DirectShow],get_ErrorCorrection method, IAMNetShowExProps.get_ErrorCorrection, IAMNetShowExProps::get_ErrorCorrection, IAMNetShowExPropsget_ErrorCorrection, dshow.iamnetshowexprops_get_errorcorrection, get_ErrorCorrection, get_ErrorCorrection method [DirectShow], get_ErrorCorrection method [DirectShow],IAMNetShowExProps interface, qnetwork/IAMNetShowExProps::get_ErrorCorrection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Qnetwork.h
api_name:
 - IAMNetShowExProps.get_ErrorCorrection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMNetShowExProps::get_ErrorCorrection


## -description



The <code>get_ErrorCorrection</code> method retrieves the current error correction method.




## -parameters




### -param pbstrErrorCorrection

Pointer to a variable that receives a string describing the error correction method.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/e68959dc-1a79-4e2c-aeaf-3febcb9c09ce">IAMNetShowExProps Interface</a>
 

 

