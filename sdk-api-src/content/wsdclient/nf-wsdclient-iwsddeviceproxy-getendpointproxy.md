---
UID: NF:wsdclient.IWSDDeviceProxy.GetEndpointProxy
title: IWSDDeviceProxy::GetEndpointProxy method
author: windows-driver-content
description: Retrieves the endpoint proxy for the device.
old-location: ncd\iwsddeviceproxy_getendpointproxy.htm
old-project: WsdApi
ms.assetid: 088c14a7-f2aa-4415-a056-a0c725602938
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetEndpointProxy method, GetEndpointProxy method, IWSDDeviceProxy interface, GetEndpointProxy,IWSDDeviceProxy.GetEndpointProxy, IWSDDeviceProxy, IWSDDeviceProxy interface, GetEndpointProxy method, IWSDDeviceProxy::GetEndpointProxy, ncd.iwsddeviceproxy_getendpointproxy, wsdclient/IWSDDeviceProxy::GetEndpointProxy
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDDeviceProxy.GetEndpointProxy
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceProxy::GetEndpointProxy method


## -description


Retrieves the endpoint proxy for the device.


## -parameters




### -param ppProxy [out]

An <a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a> interface that implements a device services messaging proxy for this device.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppProxy</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

