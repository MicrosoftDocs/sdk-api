---
UID: NF:wsdclient.IWSDAsyncResult.SetWaitHandle
title: IWSDAsyncResult::SetWaitHandle
author: windows-sdk-content
description: Specifies a wait handle to set when the operation completes.
old-location: ncd\iwsdasyncresult_setwaithandle_method.htm
old-project: wsdapi
ms.assetid: d7196785-0e9c-4320-a14e-60457f72c66b
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: IWSDAsyncResult interface,SetWaitHandle method, IWSDAsyncResult.SetWaitHandle, IWSDAsyncResult::SetWaitHandle, SetWaitHandle, SetWaitHandle method, SetWaitHandle method,IWSDAsyncResult interface, ncd.iwsdasyncresult_setwaithandle_method, wsdclient/IWSDAsyncResult::SetWaitHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDAsyncResult.SetWaitHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDAsyncResult::SetWaitHandle


## -description


Specifies a wait handle to set when the operation completes.


## -parameters




### -param hWaitHandle [in]

The wait handle to set.


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>hWaitHandle</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -remarks



Do not close <i>hWaitHandle</i> until after the asynchronous operation has completed.




## -see-also




<a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a>
 

 

