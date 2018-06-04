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

# WMPCallbackNotification enumeration


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPCallbackNotification</b> enumeration defines states for use by the <b>IWMPContentPartnerCallback::Notify</b> callback function.




## -enum-fields




### -field wmpcnLoginStateChange

The user has either signed in or signed out.


### -field wmpcnAuthResult

The notification contains the result of an authentication attempt.


### -field wmpcnLicenseUpdated

A license was updated for a content item.


### -field wmpcnNewCatalogAvailable

A new catalog or update is available for download.


### -field wmpcnNewPluginAvailable

A new plug-in or update is available for download.


### -field wmpcnDisableRadioSkipping

Disable radio skipping in Windows Media Player.


## -see-also




<a href="https://msdn.microsoft.com/7359585f-6e8f-498f-a5a2-230265bae147">Enumerations for Type 1 Online Stores</a>
 

 

