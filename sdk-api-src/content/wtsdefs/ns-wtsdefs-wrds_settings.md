---
UID: NS:wtsdefs._WRDS_SETTINGS
title: WRDS_SETTINGS (wtsdefs.h)
description: Contains policy-related setting information for a remote session.
helpviewer_keywords: ["*PWRDS_SETTINGS","PWRDS_SETTINGS","PWRDS_SETTINGS structure pointer [Remote Desktop Services]","WRDS_SETTINGS","WRDS_SETTINGS structure [Remote Desktop Services]","termserv.wrds_settings","wtsdefs/PWRDS_SETTINGS","wtsdefs/WRDS_SETTINGS"]
old-location: termserv\wrds_settings.htm
tech.root: TermServ
ms.assetid: 38AD33F9-F955-4906-90E2-3FE5261A3E58
ms.date: 12/05/2018
ms.keywords: '*PWRDS_SETTINGS, PWRDS_SETTINGS, PWRDS_SETTINGS structure pointer [Remote Desktop Services], WRDS_SETTINGS, WRDS_SETTINGS structure [Remote Desktop Services], termserv.wrds_settings, wtsdefs/PWRDS_SETTINGS, wtsdefs/WRDS_SETTINGS'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WRDS_SETTINGS, *PWRDS_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_SETTINGS
 - wtsdefs/_WRDS_SETTINGS
 - PWRDS_SETTINGS
 - wtsdefs/PWRDS_SETTINGS
 - WRDS_SETTINGS
 - wtsdefs/WRDS_SETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WRDS_SETTINGS
---

# WRDS_SETTINGS structure


## -description

Contains policy-related setting information for a remote session.

This structure is used in the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings">IWRdsProtocolSettings</a> interface and the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize">Initialize</a> method of the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a> interface.

## -struct-fields

### -field WRdsSettingType

The category of settings contained (machine group policy, user group policy, or user security accounts manager).

### -field WRdsSettingLevel

The setting level.

### -field WRdsSetting

A structure that contains the policy setting states and values.

A structure that contains the policy setting states and values.


