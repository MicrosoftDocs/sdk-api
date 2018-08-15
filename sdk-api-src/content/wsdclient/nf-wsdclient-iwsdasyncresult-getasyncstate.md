---
UID: NF:wsdclient.IWSDAsyncResult.GetAsyncState
title: IWSDAsyncResult::GetAsyncState
author: windows-sdk-content
description: Gets the state of the asynchronous operation.
old-location: ncd\iwsdasyncresult_getasyncstate_method.htm
old-project: wsdapi
ms.assetid: 4f4115bd-748e-41cd-928f-3dd3a354d336
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAsyncState, GetAsyncState method, GetAsyncState method,IWSDAsyncResult interface, IWSDAsyncResult interface,GetAsyncState method, IWSDAsyncResult.GetAsyncState, IWSDAsyncResult::GetAsyncState, ncd.iwsdasyncresult_getasyncstate_method, wsdclient/IWSDAsyncResult::GetAsyncState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.redist: 
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
 - IWSDAsyncResult.GetAsyncState
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDAsyncResult::GetAsyncState


## -description


Gets the state of the asynchronous operation.


## -parameters




### -param ppAsyncState [out]

User-defined state information.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAsyncState</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a>
 

 

