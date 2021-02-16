---
UID: NE:http._HTTP_QOS_SETTING_TYPE
title: HTTP_QOS_SETTING_TYPE (http.h)
description: Identifies the type of a QOS setting contained in a HTTP_QOS_SETTING_INFO structure.
helpviewer_keywords: ["*PHTTP_QOS_SETTING_TYPE","*PHTTP_QOS_SETTING_TYPE enumeration [HTTP]","HTTP_QOS_SETTING_TYPE","HTTP_QOS_SETTING_TYPE enumeration [HTTP]","HttpQosSettingTypeBandwidth","HttpQosSettingTypeConnectionLimit","HttpQosSettingTypeFlowRate","http.http_qos_setting_type","http/*PHTTP_QOS_SETTING_TYPE","http/HTTP_QOS_SETTING_TYPE","http/HttpQosSettingTypeBandwidth","http/HttpQosSettingTypeConnectionLimit","http/HttpQosSettingTypeFlowRate"]
old-location: http\http_qos_setting_type.htm
tech.root: http
ms.assetid: d1593670-9f5c-48a9-93d9-d5ff744cfc8b
ms.date: 12/05/2018
ms.keywords: '*PHTTP_QOS_SETTING_TYPE, *PHTTP_QOS_SETTING_TYPE enumeration [HTTP], HTTP_QOS_SETTING_TYPE, HTTP_QOS_SETTING_TYPE enumeration [HTTP], HttpQosSettingTypeBandwidth, HttpQosSettingTypeConnectionLimit, HttpQosSettingTypeFlowRate, http.http_qos_setting_type, http/*PHTTP_QOS_SETTING_TYPE, http/HTTP_QOS_SETTING_TYPE, http/HttpQosSettingTypeBandwidth, http/HttpQosSettingTypeConnectionLimit, http/HttpQosSettingTypeFlowRate'
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
targetos: Windows
req.typenames: HTTP_QOS_SETTING_TYPE, *PHTTP_QOS_SETTING_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_QOS_SETTING_TYPE
 - http/_HTTP_QOS_SETTING_TYPE
 - PHTTP_QOS_SETTING_TYPE
 - http/PHTTP_QOS_SETTING_TYPE
 - HTTP_QOS_SETTING_TYPE
 - http/HTTP_QOS_SETTING_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_QOS_SETTING_TYPE
---

# HTTP_QOS_SETTING_TYPE enumeration


## -description

The <b>HTTP_QOS_SETTING_TYPE</b> enumeration identifies the type of a QOS setting contained in a <a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a> structure.

## -enum-fields

### -field HttpQosSettingTypeBandwidth

The setting is a bandwidth limit represented by a <a href="/windows/desktop/api/http/ns-http-http_bandwidth_limit_info">HTTP_BANDWIDTH_LIMIT_INFO</a> structure.

### -field HttpQosSettingTypeConnectionLimit

The setting is a connection limit represented by a <a href="/windows/desktop/api/http/ns-http-http_connection_limit_info">HTTP_CONNECTION_LIMIT_INFO</a> structure.

### -field HttpQosSettingTypeFlowRate

A flow rate represented by <a href="/windows/desktop/api/http/ns-http-http_flowrate_info">HTTP_FLOWRATE_INFO</a>.

<div class="alert"><b>Note</b>  Windows Server 2008 R2 and Windows 7 only.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a>