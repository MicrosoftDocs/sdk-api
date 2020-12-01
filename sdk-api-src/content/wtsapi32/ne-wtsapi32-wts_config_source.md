---
UID: NE:wtsapi32._WTS_CONFIG_SOURCE
title: WTS_CONFIG_SOURCE (wtsapi32.h)
description: Specifies the source of configuration information returned by the WTSQueryUserConfig function.
helpviewer_keywords: ["WTSUserConfigSourceSAM","WTS_CONFIG_SOURCE","WTS_CONFIG_SOURCE enumeration [Remote Desktop Services]","termserv.wts_config_source","wtsapi32/WTSUserConfigSourceSAM","wtsapi32/WTS_CONFIG_SOURCE"]
old-location: termserv\wts_config_source.htm
tech.root: TermServ
ms.assetid: 2e1f45d9-dc89-4848-9ba5-e6d54b2a7737
ms.date: 12/05/2018
ms.keywords: WTSUserConfigSourceSAM, WTS_CONFIG_SOURCE, WTS_CONFIG_SOURCE enumeration [Remote Desktop Services], termserv.wts_config_source, wtsapi32/WTSUserConfigSourceSAM, wtsapi32/WTS_CONFIG_SOURCE
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_CONFIG_SOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_CONFIG_SOURCE
 - wtsapi32/_WTS_CONFIG_SOURCE
 - WTS_CONFIG_SOURCE
 - wtsapi32/WTS_CONFIG_SOURCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_CONFIG_SOURCE
---

# WTS_CONFIG_SOURCE enumeration


## -description

Specifies the  source of configuration information returned by the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a> function. This enumeration type is used in the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsuserconfiga">WTSUSERCONFIG</a> structure.

## -enum-fields

### -field WTSUserConfigSourceSAM

The configuration information came from the Security Accounts Manager (SAM) database.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsuserconfiga">WTSUSERCONFIG</a>