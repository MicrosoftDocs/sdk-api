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
 

 

