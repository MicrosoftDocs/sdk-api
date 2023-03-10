---
UID: NS:wcmapi._WCM_POLICY_VALUE
title: WCM_POLICY_VALUE (wcmapi.h)
description: Contains information about the current value of a policy.
helpviewer_keywords: ["*PWCM_POLICY_VALUE","PWCM_POLICY_VALUE","PWCM_POLICY_VALUE structure pointer [Windows Connection Manager]","WCM_POLICY_VALUE","WCM_POLICY_VALUE structure [Windows Connection Manager]","wcm.wcm_policy_value","wcmapi/PWCM_POLICY_VALUE","wcmapi/WCM_POLICY_VALUE"]
old-location: wcm\wcm_policy_value.htm
tech.root: wcm
ms.assetid: 0f259661-723b-4c76-8652-c86e0b8c9ebf
ms.date: 12/05/2018
ms.keywords: '*PWCM_POLICY_VALUE, PWCM_POLICY_VALUE, PWCM_POLICY_VALUE structure pointer [Windows Connection Manager], WCM_POLICY_VALUE, WCM_POLICY_VALUE structure [Windows Connection Manager], wcm.wcm_policy_value, wcmapi/PWCM_POLICY_VALUE, wcmapi/WCM_POLICY_VALUE'
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
req.typenames: WCM_POLICY_VALUE, *PWCM_POLICY_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WCM_POLICY_VALUE
 - wcmapi/_WCM_POLICY_VALUE
 - PWCM_POLICY_VALUE
 - wcmapi/PWCM_POLICY_VALUE
 - WCM_POLICY_VALUE
 - wcmapi/WCM_POLICY_VALUE
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
 - WCM_POLICY_VALUE
---

# WCM_POLICY_VALUE structure


## -description

The <b>WCM_POLICY_VALUE</b> structure contains information about the current value of a policy.

## -struct-fields

### -field fValue

Type: <b>BOOL</b>

True if the policy is enabled; otherwise, false.

### -field fIsGroupPolicy

Type: <b>BOOL</b>

True if the current value was provided by Group Policy; otherwise, false.

