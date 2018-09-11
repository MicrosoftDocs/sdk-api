---
UID: NF:wsdclient.IWSDEndpointProxy.SendTwoWayRequestAsync
title: IWSDEndpointProxy::SendTwoWayRequestAsync
author: windows-sdk-content
description: Sends a two-way request message using an asynchronous call pattern.
old-location: ncd\iwsdendpointproxy_sendtwowayrequestasync.htm
tech.root: WsdApi
ms.assetid: cf175e79-9df2-4481-b784-e2cc40e34222
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDEndpointProxy interface,SendTwoWayRequestAsync method, IWSDEndpointProxy.SendTwoWayRequestAsync, IWSDEndpointProxy::SendTwoWayRequestAsync, SendTwoWayRequestAsync, SendTwoWayRequestAsync method, SendTwoWayRequestAsync method,IWSDEndpointProxy interface, ncd.iwsdendpointproxy_sendtwowayrequestasync, wsdclient/IWSDEndpointProxy::SendTwoWayRequestAsync
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
 - IWSDEndpointProxy.SendTwoWayRequestAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDEndpointProxy::SendTwoWayRequestAsync


## -description


Sends a two-way request message using an asynchronous call pattern.


## -parameters




### -param pBody [in]

The body of the message.


### -param pOperation [in]

Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation to perform. 



### -param pAsyncState [in]

Anonymous data passed to <i>pCallback</i> when the operation has completed.  This data is used to associate a client object with the pending operation. This parameter may be  optional.


### -param pCallback [in]

Reference to an <a href="https://msdn.microsoft.com/24108143-55b7-4098-a4cc-025dfdfd054a">IWSDAsyncCallback</a> object which performs the message status callback notification. This parameter may be  optional.


### -param pResult [out]

Reference to an <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> object that specifies the results of the operation. 



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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pOperation</i> or <i>pResult</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



This method is normally only called by generated proxy code.




## -see-also




<a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a>
 

 

