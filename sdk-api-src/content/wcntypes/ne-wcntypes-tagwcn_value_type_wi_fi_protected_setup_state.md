---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
title: tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
author: windows-sdk-content
description: WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration.
old-location: wcn\wcn_value_type_wi_fi_protected_setup_state.htm
old-project: wcn
ms.assetid: b42d6e7c-9dba-4205-97bc-0107c168b754
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WCN_VALUE_SS_CONFIGURED, WCN_VALUE_SS_NOT_CONFIGURED, WCN_VALUE_SS_RESERVED00, WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE, WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration [Windows Connect Now], tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE, wcn.wcn_value_type_wi_fi_protected_setup_state, wcntypes/WCN_VALUE_SS_CONFIGURED, wcntypes/WCN_VALUE_SS_NOT_CONFIGURED, wcntypes/WCN_VALUE_SS_RESERVED00, wcntypes/WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wcntypes.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wcndevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wcntypes.h
api_name:
 - WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration


## -description


The <b>WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE</b> enumeration defines values that indicate if a device is configured.


## -enum-fields




### -field WCN_VALUE_SS_RESERVED00

This value is reserved.


### -field WCN_VALUE_SS_NOT_CONFIGURED

The device is not configured.


### -field WCN_VALUE_SS_CONFIGURED

The device is configured. 


## -remarks



A device is considered 'not configured' if it is using factory default wireless settings. If the wireless settings have been customized by the user, the device is considered to be 'configured'. A factory reset will restore the device to a 'not configured' state.




## -see-also




<a href="https://msdn.microsoft.com/214b64c3-b1f0-46b1-b52a-b1df1bb40cf7">WCN_ATTRIBUTE_TYPE</a>
 

 

