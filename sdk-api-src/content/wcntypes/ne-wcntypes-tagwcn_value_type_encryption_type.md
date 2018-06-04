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

# tagWCN_VALUE_TYPE_ENCRYPTION_TYPE enumeration


## -description


The <b>WCN_VALUE_TYPE_ENCRYPTION_TYPE</b> enumeration defines the supported WLAN encryption types.


## -enum-fields




### -field WCN_VALUE_ET_NONE

Specifies support for unsecured wireless activity.


### -field WCN_VALUE_ET_WEP

Specifies support for the Wired Equivalent Privacy (WEP) encryption method.

<div class="alert"><b>Note</b>  Not available for WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_ET_TKIP

Specifies support for the Temporal Key Integrity Protocol (TKIP) encryption method.

<div class="alert"><b>Note</b>  Not available for WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_ET_AES

Specifies support for the Advanced Encryption Standard (AES) encryption method.


### -field WCN_VALUE_ET_TKIP_AES_MIXED

Specifies support for WPAPSK/WPA2PSK mixed-mode encryption.

<div class="alert"><b>Note</b>  Not supported in WPS 1.0. Only available  in Windows 8.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/214b64c3-b1f0-46b1-b52a-b1df1bb40cf7">WCN_ATTRIBUTE_TYPE</a>
 

 

