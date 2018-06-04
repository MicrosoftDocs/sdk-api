---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _HTTP_QOS_SETTING_TYPE enumeration


## -description


The <b>HTTP_QOS_SETTING_TYPE</b> enumeration identifies the type of a QOS setting contained in a <a href="https://msdn.microsoft.com/6c220063-02d0-44c0-b3a3-e7bfd5c57e1f">HTTP_QOS_SETTING_INFO</a> structure.


## -enum-fields




### -field HttpQosSettingTypeBandwidth

The setting is a bandwidth limit represented by a <a href="https://msdn.microsoft.com/34c85ecf-1eb4-4f0d-a081-4b9feeb8dd15">HTTP_BANDWIDTH_LIMIT_INFO</a> structure.


### -field HttpQosSettingTypeConnectionLimit

The setting is a connection limit represented by a <a href="https://msdn.microsoft.com/6d2c1eeb-d248-4ca5-80b3-5c9f69ce8b9b">HTTP_CONNECTION_LIMIT_INFO</a> structure.


### -field HttpQosSettingTypeFlowRate

A flow rate represented by <a href="https://msdn.microsoft.com/5b52ef5b-dc82-4a87-9204-d32134074c31">HTTP_FLOWRATE_INFO</a>.

<div class="alert"><b>Note</b>  Windows Server 2008 R2 and Windows 7 only.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/6c220063-02d0-44c0-b3a3-e7bfd5c57e1f">HTTP_QOS_SETTING_INFO</a>
 

 

