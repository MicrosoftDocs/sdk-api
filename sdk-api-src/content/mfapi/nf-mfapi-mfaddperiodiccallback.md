---
UID: NF:mfapi.MFAddPeriodicCallback
title: MFAddPeriodicCallback function
author: windows-sdk-content
description: Sets a callback function to be called at a fixed interval.
old-location: mf\mfaddperiodiccallback.htm
old-project: medfound
ms.assetid: e5898fc8-72e9-45cc-8e85-4410ed7cc512
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFAddPeriodicCallback, MFAddPeriodicCallback function [Media Foundation], e5898fc8-72e9-45cc-8e85-4410ed7cc512, mf.mfaddperiodiccallback, mfapi/MFAddPeriodicCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFAddPeriodicCallback
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFAddPeriodicCallback function


## -description



Sets a callback function to be called at a fixed interval.




## -parameters




### -param Callback [in]

Pointer to the callback function, of type <a href="https://msdn.microsoft.com/9449fa04-867c-4f27-a05c-ff0d6e912c53">MFPERIODICCALLBACK</a>.


### -param pContext [in]

Pointer to a caller-provided object that implements <b>IUnknown</b>, or <b>NULL</b>. This parameter is passed to the callback function.


### -param pdwKey [out]

Receives a key that can be used to cancel the callback. To cancel the callback, call <a href="https://msdn.microsoft.com/e70cdad3-c330-4368-8ef8-d616157b5e72">MFRemovePeriodicCallback</a> and pass this key as the <i>dwKey</i> parameter.


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



To get the timer interval for the periodic callback, call <a href="https://msdn.microsoft.com/19d7ae7e-7ae3-474d-8111-3b60b9adb918">MFGetTimerPeriodicity</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

