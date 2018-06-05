---
UID: NF:wsdhost.IWSDDeviceHostNotify.GetService
title: IWSDDeviceHostNotify::GetService
author: windows-sdk-content
description: Retrieves a service object that is not currently registered.
old-location: ncd\iwsddevicehostnotify_getservice_method.htm
old-project: WsdApi
ms.assetid: 5222b99a-b438-4775-91f0-8bcc7d3b73e8
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetService, GetService method, GetService method,IWSDDeviceHostNotify interface, IWSDDeviceHostNotify interface,GetService method, IWSDDeviceHostNotify.GetService, IWSDDeviceHostNotify::GetService, ncd.iwsddevicehostnotify_getservice_method, wsdhost/IWSDDeviceHostNotify::GetService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDDeviceHostNotify.GetService
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceHostNotify::GetService


## -description


Retrieves a service object that is not currently registered.




## -parameters




### -param pszServiceId [in]

The ID of the service to be produced. 



### -param ppService [out]

 A reference to an <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> object for the specified service. 



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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e68e347d-5251-4931-bbcc-7a92b46bf4bd">IWSDDeviceHostNotify</a>
 

 

