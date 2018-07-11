---
UID: NF:mfidl.IMFRemoteProxy.GetRemoteHost
title: IMFRemoteProxy::GetRemoteHost
author: windows-sdk-content
description: Retrieves a pointer to the object that is hosting this proxy.
old-location: mf\imfremoteproxy_getremotehost.htm
old-project: medfound
ms.assetid: e3a4407a-d8e4-4c7b-81da-88d63e0d77b8
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRemoteHost, GetRemoteHost method [Media Foundation], GetRemoteHost method [Media Foundation],IMFRemoteProxy interface, IMFRemoteProxy interface [Media Foundation],GetRemoteHost method, IMFRemoteProxy.GetRemoteHost, IMFRemoteProxy::GetRemoteHost, e3a4407a-d8e4-4c7b-81da-88d63e0d77b8, mf.imfremoteproxy_getremotehost, mfidl/IMFRemoteProxy::GetRemoteHost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRemoteProxy.GetRemoteHost
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFRemoteProxy::GetRemoteHost


## -description



Retrieves a pointer to the object that is hosting this proxy.




## -parameters




### -param riid [in]

Interface identifier (IID) of the requested interface.


### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
 




## -see-also




<a href="https://msdn.microsoft.com/46af5ba7-c362-4cfd-ae6d-b698c6403a65">IMFRemoteProxy</a>
 

 

