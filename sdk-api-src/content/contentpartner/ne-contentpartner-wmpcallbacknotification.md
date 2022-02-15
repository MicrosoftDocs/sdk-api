---
UID: NE:contentpartner.WMPCallbackNotification
title: WMPCallbackNotification (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["WMPCallbackNotification","WMPCallbackNotification enumeration [Windows Media Player]","contentpartner/WMPCallbackNotification","contentpartner/wmpcnAuthResult","contentpartner/wmpcnDisableRadioSkipping","contentpartner/wmpcnLicenseUpdated","contentpartner/wmpcnLoginStateChange","contentpartner/wmpcnNewCatalogAvailable","contentpartner/wmpcnNewPluginAvailable","enumeration [Windows Media Player]","wmp.wmpcallbacknotification","wmpcnAuthResult","wmpcnDisableRadioSkipping","wmpcnLicenseUpdated","wmpcnLoginStateChange","wmpcnNewCatalogAvailable","wmpcnNewPluginAvailable"]
old-location: wmp\wmpcallbacknotification.htm
tech.root: WMP
ms.assetid: 6c0ba35f-a484-4d00-be42-af5114086250
ms.date: 12/05/2018
ms.keywords: WMPCallbackNotification, WMPCallbackNotification enumeration [Windows Media Player], contentpartner/WMPCallbackNotification, contentpartner/wmpcnAuthResult, contentpartner/wmpcnDisableRadioSkipping, contentpartner/wmpcnLicenseUpdated, contentpartner/wmpcnLoginStateChange, contentpartner/wmpcnNewCatalogAvailable, contentpartner/wmpcnNewPluginAvailable, enumeration [Windows Media Player], wmp.wmpcallbacknotification, wmpcnAuthResult, wmpcnDisableRadioSkipping, wmpcnLicenseUpdated, wmpcnLoginStateChange, wmpcnNewCatalogAvailable, wmpcnNewPluginAvailable
req.header: contentpartner.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMPCallbackNotification
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPCallbackNotification
 - contentpartner/WMPCallbackNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPCallbackNotification
---

# WMPCallbackNotification enumeration


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPCallbackNotification</b> enumeration defines states for use by the <b>IWMPContentPartnerCallback::Notify</b> callback function.

## -enum-fields

### -field wmpcnLoginStateChange:1

The user has either signed in or signed out.

### -field wmpcnAuthResult:2

The notification contains the result of an authentication attempt.

### -field wmpcnLicenseUpdated:3

A license was updated for a content item.

### -field wmpcnNewCatalogAvailable:4

A new catalog or update is available for download.

### -field wmpcnNewPluginAvailable:5

A new plug-in or update is available for download.

### -field wmpcnDisableRadioSkipping:6

Disable radio skipping in Windows Media Player.

## -see-also

<a href="/windows/desktop/WMP/enumerations-for-type-1-online-stores">Enumerations for Type 1 Online Stores</a>
