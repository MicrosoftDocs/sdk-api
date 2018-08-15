---
UID: NS:wcmapi._WCM_POLICY_VALUE
title: "_WCM_POLICY_VALUE"
author: windows-sdk-content
description: Contains information about the current value of a policy.
old-location: wcm\wcm_policy_value.htm
old-project: wcm
ms.assetid: 0f259661-723b-4c76-8652-c86e0b8c9ebf
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PWCM_POLICY_VALUE, PWCM_POLICY_VALUE, PWCM_POLICY_VALUE structure pointer [Windows Connection Manager], WCM_POLICY_VALUE, WCM_POLICY_VALUE structure [Windows Connection Manager], _WCM_POLICY_VALUE, wcm.wcm_policy_value, wcmapi/PWCM_POLICY_VALUE, wcmapi/WCM_POLICY_VALUE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wcmapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WCM_POLICY_VALUE, *PWCM_POLICY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_POLICY_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WCM_POLICY_VALUE structure


## -description


The <b>WCM_POLICY_VALUE</b> structure contains information about the current value of a policy.


## -struct-fields




### -field fValue

Type: <b>BOOL</b>

True if the policy is enabled; otherwise, false.


### -field fIsGroupPolicy

Type: <b>BOOL</b>

True if the current value was provided by Group Policy; otherwise, false.

