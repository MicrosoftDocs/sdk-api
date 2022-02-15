---
UID: NE:wcmapi._WCM_CONNECTION_COST_SOURCE
title: WCM_CONNECTION_COST_SOURCE (wcmapi.h)
description: Specifies the source that provides connection cost information.
helpviewer_keywords: ["*PWCM_CONNECTION_COST_SOURCE","PWCM_CONNECTION_COST_SOURCE","PWCM_CONNECTION_COST_SOURCE enumeration pointer [Windows Connection Manager]","WCM_CONNECTION_COST_SOURCE","WCM_CONNECTION_COST_SOURCE enumeration [Windows Connection Manager]","WCM_CONNECTION_COST_SOURCE_DEFAULT","WCM_CONNECTION_COST_SOURCE_GP","WCM_CONNECTION_COST_SOURCE_OPERATOR","WCM_CONNECTION_COST_SOURCE_USER","wcm.wcm_connection_cost_source","wcmapi/PWCM_CONNECTION_COST_SOURCE","wcmapi/WCM_CONNECTION_COST_SOURCE","wcmapi/WCM_CONNECTION_COST_SOURCE_DEFAULT","wcmapi/WCM_CONNECTION_COST_SOURCE_GP","wcmapi/WCM_CONNECTION_COST_SOURCE_OPERATOR","wcmapi/WCM_CONNECTION_COST_SOURCE_USER"]
old-location: wcm\wcm_connection_cost_source.htm
tech.root: wcm
ms.assetid: cd9e5562-dd50-46fc-be11-0ea89e6933c0
ms.date: 12/05/2018
ms.keywords: '*PWCM_CONNECTION_COST_SOURCE, PWCM_CONNECTION_COST_SOURCE, PWCM_CONNECTION_COST_SOURCE enumeration pointer [Windows Connection Manager], WCM_CONNECTION_COST_SOURCE, WCM_CONNECTION_COST_SOURCE enumeration [Windows Connection Manager], WCM_CONNECTION_COST_SOURCE_DEFAULT, WCM_CONNECTION_COST_SOURCE_GP, WCM_CONNECTION_COST_SOURCE_OPERATOR, WCM_CONNECTION_COST_SOURCE_USER, wcm.wcm_connection_cost_source, wcmapi/PWCM_CONNECTION_COST_SOURCE, wcmapi/WCM_CONNECTION_COST_SOURCE, wcmapi/WCM_CONNECTION_COST_SOURCE_DEFAULT, wcmapi/WCM_CONNECTION_COST_SOURCE_GP, wcmapi/WCM_CONNECTION_COST_SOURCE_OPERATOR, wcmapi/WCM_CONNECTION_COST_SOURCE_USER'
req.header: wcmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WCM_CONNECTION_COST_SOURCE, *PWCM_CONNECTION_COST_SOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WCM_CONNECTION_COST_SOURCE
 - wcmapi/_WCM_CONNECTION_COST_SOURCE
 - PWCM_CONNECTION_COST_SOURCE
 - wcmapi/PWCM_CONNECTION_COST_SOURCE
 - WCM_CONNECTION_COST_SOURCE
 - wcmapi/WCM_CONNECTION_COST_SOURCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_CONNECTION_COST_SOURCE
---

# WCM_CONNECTION_COST_SOURCE enumeration


## -description

The <b>WCM_CONNECTION_COST_SOURCE</b> enumerated type specifies the source that provides connection cost information.

## -enum-fields

### -field WCM_CONNECTION_COST_SOURCE_DEFAULT:0

Default source.

### -field WCM_CONNECTION_COST_SOURCE_GP:1

The source for the connection cost  is Group Policy.

### -field WCM_CONNECTION_COST_SOURCE_USER:2

The source for the connection cost is the user.

### -field WCM_CONNECTION_COST_SOURCE_OPERATOR:3

The source for the connection cost  is the operator.

