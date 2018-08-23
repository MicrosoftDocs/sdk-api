---
UID: NE:contentpartner.WMPCallbackNotification
title: WMPCallbackNotification
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\wmpcallbacknotification.htm
old-project: WMP
ms.assetid: 6c0ba35f-a484-4d00-be42-af5114086250
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WMPCallbackNotification, WMPCallbackNotification enumeration [Windows Media Player], contentpartner/WMPCallbackNotification, contentpartner/wmpcnAuthResult, contentpartner/wmpcnDisableRadioSkipping, contentpartner/wmpcnLicenseUpdated, contentpartner/wmpcnLoginStateChange, contentpartner/wmpcnNewCatalogAvailable, contentpartner/wmpcnNewPluginAvailable, enumeration [Windows Media Player], wmp.wmpcallbacknotification, wmpcnAuthResult, wmpcnDisableRadioSkipping, wmpcnLicenseUpdated, wmpcnLoginStateChange, wmpcnNewCatalogAvailable, wmpcnNewPluginAvailable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: contentpartner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
tech.root: 
req.typenames: WMPCallbackNotification
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPCallbackNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd562861(v=VS.85).aspx">Enumerations for Type 1 Online Stores</a>
 

 

