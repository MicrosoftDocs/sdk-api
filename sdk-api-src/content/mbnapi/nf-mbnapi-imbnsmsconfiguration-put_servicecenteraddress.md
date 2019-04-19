---
UID: NF:mbnapi.IMbnSmsConfiguration.put_ServiceCenterAddress
title: IMbnSmsConfiguration::put_ServiceCenterAddress (mbnapi.h)
author: windows-sdk-content
description: SMS default Service Center address.
old-location: mbn\imbnsmsconfiguration_servicecenteraddress.htm
tech.root: mbn
ms.assetid: 10f34db2-2f1b-4e51-96c7-70a080804fd4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnSmsConfiguration interface [Microsoft Broadband Networks],ServiceCenterAddress property, IMbnSmsConfiguration.ServiceCenterAddress, IMbnSmsConfiguration.put_ServiceCenterAddress, IMbnSmsConfiguration::ServiceCenterAddress, IMbnSmsConfiguration::get_ServiceCenterAddress, IMbnSmsConfiguration::put_ServiceCenterAddress, ServiceCenterAddress property [Microsoft Broadband Networks], ServiceCenterAddress property [Microsoft Broadband Networks],IMbnSmsConfiguration interface, mbn.imbnsmsconfiguration_servicecenteraddress, mbnapi/IMbnSmsConfiguration::ServiceCenterAddress, mbnapi/IMbnSmsConfiguration::get_ServiceCenterAddress, mbnapi/IMbnSmsConfiguration::put_ServiceCenterAddress, put_ServiceCenterAddress
ms.topic: method
req.header: mbnapi.h
req.include-header: Mbnapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSmsConfiguration.ServiceCenterAddress
 - IMbnSmsConfiguration.get_ServiceCenterAddress
 - IMbnSmsConfiguration.put_ServiceCenterAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnSmsConfiguration::put_ServiceCenterAddress


## -description


SMS default Service Center address.

This property is read/write.


## -parameters


## -remarks




When setting <i>scAddress</i>, the calling application must use either of these formats.

<ul>
<li>"+ &lt;International Country Code&gt; &lt;SMS Service Center Number&gt;\0"</li>
<li>"&lt;SMS Service Center Number&gt;\0"</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>
 

 

