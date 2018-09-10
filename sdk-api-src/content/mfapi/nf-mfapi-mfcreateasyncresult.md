---
UID: NF:mfapi.MFCreateAsyncResult
title: MFCreateAsyncResult function
author: windows-sdk-content
description: Creates an asynchronous result object. Use this function if you are implementing an asynchronous method.
old-location: mf\mfcreateasyncresult.htm
tech.root: medfound
ms.assetid: 6ff773a9-961e-4a5e-ad37-46234022c575
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 6ff773a9-961e-4a5e-ad37-46234022c575, MFCreateAsyncResult, MFCreateAsyncResult function [Media Foundation], mf.mfcreateasyncresult, mfapi/MFCreateAsyncResult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateAsyncResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateAsyncResult function


## -description



Creates an asynchronous result object. Use this function if you are implementing an asynchronous method.




## -parameters




### -param punkObject

Pointer to the object stored in the asynchronous result. This pointer is returned by the <a href="https://msdn.microsoft.com/b4b871ff-370d-4a37-9fe4-91d1805890eb">IMFAsyncResult::GetObject</a> method. This parameter can be <b>NULL</b>.


### -param pCallback

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface. This interface is implemented by the caller of the asynchronous method.


### -param punkState

Pointer to the <b>IUnknown</b> interface of a state object. This value is provided by the caller of the asynchronous method. This parameter can be <b>NULL</b>.


### -param ppAsyncResult

Receives a pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



To invoke the callback specified in <i>pCallback</i>, call the <a href="https://msdn.microsoft.com/28832d50-9b15-4eb0-96f9-2032d4edcaf4">MFInvokeCallback</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

