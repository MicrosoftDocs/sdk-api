---
UID: NF:wsdclient.IWSDServiceProxy.SetEventingStatusCallback
title: IWSDServiceProxy::SetEventingStatusCallback
author: windows-sdk-content
description: Sets or clears the eventing status callback.
old-location: ncd\iwsdserviceproxy_seteventingstatuscallback.htm
tech.root: wsdapi
ms.assetid: 0a924df4-93a7-4443-a384-0a89d5d90509
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDServiceProxy interface,SetEventingStatusCallback method, IWSDServiceProxy.SetEventingStatusCallback, IWSDServiceProxy::SetEventingStatusCallback, SetEventingStatusCallback, SetEventingStatusCallback method, SetEventingStatusCallback method,IWSDServiceProxy interface, ncd.iwsdserviceproxy_seteventingstatuscallback, wsdclient/IWSDServiceProxy::SetEventingStatusCallback
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
 - IWSDServiceProxy.SetEventingStatusCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceProxy::SetEventingStatusCallback


## -description


Sets or clears the eventing status callback.


## -parameters




### -param pStatus [in, optional]

An <a href="https://msdn.microsoft.com/04e6ea03-f9b5-48d9-940f-532bb3a85ff0">IWSDEventingStatus</a> interface that lets the client know of status changes in event subscriptions. If <b>NULL</b>, existing eventing status callbacks are cleared. 


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
Method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a>
 

 

