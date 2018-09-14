---
UID: NF:mfidl.IMFGetService.GetService
title: IMFGetService::GetService
author: windows-sdk-content
description: Retrieves a service interface.
old-location: mf\imfgetservice_getservice.htm
tech.root: medfound
ms.assetid: 4287dd1f-1718-4231-bc62-b58e0e61d688
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 4287dd1f-1718-4231-bc62-b58e0e61d688, GetService, GetService method [Media Foundation], GetService method [Media Foundation],IMFGetService interface, IMFGetService interface [Media Foundation],GetService method, IMFGetService.GetService, IMFGetService::GetService, mf.imfgetservice_getservice, mfidl/IMFGetService::GetService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFGetService.GetService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFGetService::GetService


## -description



Retrieves a service interface.




## -parameters




### -param guidService [in]

The service identifier (SID) of the service. For a list of service identifiers, see <a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>.


### -param riid [in]

The interface identifier (IID) of the interface being requested.


### -param ppvObject [out]

Receives the interface pointer. The caller must release the interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the service.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/102a1dff-8419-4f86-a145-53ce3d0123f5">IMFGetService</a>



<a href="https://msdn.microsoft.com/119e9e2f-0e26-4dfc-9c89-156b63a63640">MFGetService</a>



<a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>
 

 

