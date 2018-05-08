---
UID: NF:portabledeviceconnectapi.IConnectionRequestCallback.OnComplete
title: IConnectionRequestCallback::OnComplete
author: windows-driver-content
description: Notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed.
old-location: wpdsdk\iconnectionrequestcallback_oncomplete.htm
old-project: wpd_sdk
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IConnectionRequestCallback interface [Windows Portable Devices SDK],OnComplete method, IConnectionRequestCallback.OnComplete, IConnectionRequestCallback::OnComplete, OnComplete, OnComplete method [Windows Portable Devices SDK], OnComplete method [Windows Portable Devices SDK],IConnectionRequestCallback interface, devpkey/IConnectionRequestCallback::OnComplete, portabledeviceconnectapi/IConnectionRequestCallback::OnComplete, wpdsdk.iconnectionrequestcallback_oncomplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGuids.lib
-	PortableDeviceGuids.dll
api_name:
-	IConnectionRequestCallback.OnComplete
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IConnectionRequestCallback::OnComplete


## -description


The <b>OnComplete</b> method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed


## -parameters




### -param hrStatus [in]

The status of the request to connect or disconnect a given device.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



An application implements the <a href="https://msdn.microsoft.com/579f7a29-cd98-4d97-9f8e-9b786897df1c">IConnectionRequestCallback</a> interface to receive notifications about completed requests and to cancel pending requests.

Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.  Each request can be tracked and canceled by its application-supplied callback.  Therefore, if the application needs to send multiple requests at the same time using the same <a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a> object, each request should be passed a unique <a href="https://msdn.microsoft.com/579f7a29-cd98-4d97-9f8e-9b786897df1c">IConnectionRequestCallback</a> object as the input parameter to the <a href="https://msdn.microsoft.com/2bb5b124-3018-4619-bb8f-67fcfc8981d9">IPortableDeviceConnector::Connect</a> and <a href="https://msdn.microsoft.com/0cc104e6-5e3a-4fce-ba3b-68f3fb94196b">IPortableDeviceConnector::Disconnect</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/579f7a29-cd98-4d97-9f8e-9b786897df1c">IConnectionRequestCallback</a>
 

 

