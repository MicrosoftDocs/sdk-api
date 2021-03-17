---
UID: NS:http._HTTP_QOS_SETTING_INFO
title: HTTP_QOS_SETTING_INFO (http.h)
description: Contains information about a QOS setting.
helpviewer_keywords: ["*PHTTP_QOS_SETTING_INFO","HTTP_QOS_SETTING_INFO","HTTP_QOS_SETTING_INFO structure [HTTP]","PHTTP_QOS_SETTING_INFO","PHTTP_QOS_SETTING_INFO structure pointer [HTTP]","http.http_qos_setting_info","http/HTTP_QOS_SETTING_INFO","http/PHTTP_QOS_SETTING_INFO"]
old-location: http\http_qos_setting_info.htm
tech.root: http
ms.assetid: 6c220063-02d0-44c0-b3a3-e7bfd5c57e1f
ms.date: 12/05/2018
ms.keywords: '*PHTTP_QOS_SETTING_INFO, HTTP_QOS_SETTING_INFO, HTTP_QOS_SETTING_INFO structure [HTTP], PHTTP_QOS_SETTING_INFO, PHTTP_QOS_SETTING_INFO structure pointer [HTTP], http.http_qos_setting_info, http/HTTP_QOS_SETTING_INFO, http/PHTTP_QOS_SETTING_INFO'
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
req.typenames: HTTP_QOS_SETTING_INFO, *PHTTP_QOS_SETTING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_QOS_SETTING_INFO
 - http/_HTTP_QOS_SETTING_INFO
 - PHTTP_QOS_SETTING_INFO
 - http/PHTTP_QOS_SETTING_INFO
 - HTTP_QOS_SETTING_INFO
 - http/HTTP_QOS_SETTING_INFO
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
 - HTTP_QOS_SETTING_INFO
---

# HTTP_QOS_SETTING_INFO structure


## -description

The <b>HTTP_QOS_SETTING_INFO</b> structurecontains information about a QOS setting.

## -struct-fields

### -field QosType

An <a href="/windows/desktop/api/http/ne-http-http_qos_setting_type">HTTP_QOS_SETTING_TYPE</a> enumeration value that specifies the type of the QOS setting.

### -field QosSetting

A pointer to a structure that contains the setting.

## -see-also

<a href="/windows/desktop/api/http/ne-http-http_qos_setting_type">HTTP_QOS_SETTING_TYPE</a>