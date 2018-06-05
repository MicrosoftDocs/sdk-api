---
UID: NF:mfidl.IMFNetProxyLocatorFactory.CreateProxyLocator
title: IMFNetProxyLocatorFactory::CreateProxyLocator
author: windows-sdk-content
description: Creates an IMFNetProxyLocator interface proxy locator object based on the protocol name.
old-location: mf\imfnetproxylocatorfactory_createproxylocator.htm
old-project: medfound
ms.assetid: 0bdc03a8-a01d-453b-92b9-b39d8028b314
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 0bdc03a8-a01d-453b-92b9-b39d8028b314, CreateProxyLocator, CreateProxyLocator method [Media Foundation], CreateProxyLocator method [Media Foundation],IMFNetProxyLocatorFactory interface, IMFNetProxyLocatorFactory interface [Media Foundation],CreateProxyLocator method, IMFNetProxyLocatorFactory.CreateProxyLocator, IMFNetProxyLocatorFactory::CreateProxyLocator, mf.imfnetproxylocatorfactory_createproxylocator, mfidl/IMFNetProxyLocatorFactory::CreateProxyLocator
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFNetProxyLocatorFactory.CreateProxyLocator
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetProxyLocatorFactory::CreateProxyLocator


## -description



Creates an <a href="https://msdn.microsoft.com/2906b998-f1ca-4c65-b810-cbc360390653">IMFNetProxyLocator</a> interface proxy locator object based on the protocol name.




## -parameters




### -param pszProtocol [in]

Null-terminated wide-character string containing the protocol name (for example, RTSP or HTTP).


### -param ppProxyLocator [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/2906b998-f1ca-4c65-b810-cbc360390653">IMFNetProxyLocator</a> interface. The caller must release the interface.


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
 




## -see-also




<a href="https://msdn.microsoft.com/6dd5bf50-2d07-47c7-869e-035d7e92a6bc">IMFNetProxyLocatorFactory</a>
 

 

