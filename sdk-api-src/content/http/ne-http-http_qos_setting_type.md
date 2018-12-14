---
UID: NE:http._HTTP_QOS_SETTING_TYPE
title: HTTP_QOS_SETTING_TYPE
author: windows-sdk-content
description: Identifies the type of a QOS setting contained in a HTTP_QOS_SETTING_INFO structure.
old-location: http\http_qos_setting_type.htm
tech.root: http
ms.assetid: d1593670-9f5c-48a9-93d9-d5ff744cfc8b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PHTTP_QOS_SETTING_TYPE, *PHTTP_QOS_SETTING_TYPE enumeration [HTTP], HTTP_QOS_SETTING_TYPE, HTTP_QOS_SETTING_TYPE enumeration [HTTP], HttpQosSettingTypeBandwidth, HttpQosSettingTypeConnectionLimit, HttpQosSettingTypeFlowRate, http.http_qos_setting_type, http/*PHTTP_QOS_SETTING_TYPE, http/HTTP_QOS_SETTING_TYPE, http/HttpQosSettingTypeBandwidth, http/HttpQosSettingTypeConnectionLimit, http/HttpQosSettingTypeFlowRate"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: http.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_QOS_SETTING_TYPE
product: Windows
targetos: Windows
req.typenames: HTTP_QOS_SETTING_TYPE, *PHTTP_QOS_SETTING_TYPE
req.redist: 
---

# HTTP_QOS_SETTING_TYPE enumeration


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
 

 

