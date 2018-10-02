---
UID: NF:wsdclient.IWSDServiceProxy.UnsubscribeToOperation
title: IWSDServiceProxy::UnsubscribeToOperation
author: windows-sdk-content
description: Cancels a subscription to a notification or solicit/response event.
old-location: ncd\iwsdserviceproxy_unsubscribetooperation_method.htm
tech.root: WsdApi
ms.assetid: b306239c-95a4-4a1d-990c-193237bad275
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDServiceProxy interface,UnsubscribeToOperation method, IWSDServiceProxy.UnsubscribeToOperation, IWSDServiceProxy::UnsubscribeToOperation, UnsubscribeToOperation, UnsubscribeToOperation method, UnsubscribeToOperation method,IWSDServiceProxy interface, ncd.iwsdserviceproxy_unsubscribetooperation_method, wsdclient/IWSDServiceProxy::UnsubscribeToOperation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDServiceProxy.UnsubscribeToOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceProxy::UnsubscribeToOperation


## -description


Cancels a subscription to a notification or solicit/response event.


## -parameters




### -param pOperation [in]

Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation subscribed to. 



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
The proxy is not subscribed to the notification specified by <i>pOperation</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pOperation</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a>
 

 

