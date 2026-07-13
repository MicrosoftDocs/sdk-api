---
UID: NS:wia_xp._WIA_PROPID_TO_NAME
title: WIA_PROPID_TO_NAME (wia_xp.h)
description: Provides a quick means by which applications can look up the standard Windows Image Acquisition (WIA) property name from the WIA property ID (or vice versa).
helpviewer_keywords: ["*PWIA_PROPID_TO_NAME","PWIA_PROPID_TO_NAME","PWIA_PROPID_TO_NAME structure pointer [WIA]","WIA_PROPID_TO_NAME","WIA_PROPID_TO_NAME structure [WIA]","_wia_WIA_PROPID_TO_NAME","wia._wia_WIA_PROPID_TO_NAME","wia_xp/PWIA_PROPID_TO_NAME","wia_xp/WIA_PROPID_TO_NAME"]
old-location: wia\_wia_WIA_PROPID_TO_NAME.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_propid_to_name.htm
ms.date: 12/05/2018
ms.keywords: '*PWIA_PROPID_TO_NAME, PWIA_PROPID_TO_NAME, PWIA_PROPID_TO_NAME structure pointer [WIA], WIA_PROPID_TO_NAME, WIA_PROPID_TO_NAME structure [WIA], _wia_WIA_PROPID_TO_NAME, wia._wia_WIA_PROPID_TO_NAME, wia_xp/PWIA_PROPID_TO_NAME, wia_xp/WIA_PROPID_TO_NAME'
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WIA_PROPID_TO_NAME, *PWIA_PROPID_TO_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIA_PROPID_TO_NAME
 - wia_xp/_WIA_PROPID_TO_NAME
 - PWIA_PROPID_TO_NAME
 - wia_xp/PWIA_PROPID_TO_NAME
 - WIA_PROPID_TO_NAME
 - wia_xp/WIA_PROPID_TO_NAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wia_xp.h
api_name:
 - WIA_PROPID_TO_NAME
archived: true
---

# WIA_PROPID_TO_NAME structure


## -description

Provides a quick means by which applications can look up the standard Windows Image Acquisition (WIA) property name from the WIA property ID (or vice versa). If the <b>propid</b> does not exist in this array, it is likely not a standard WIA property. Other ways to get the property name from the property ID include using the <b>IEnumSTATPROPSTG</b> retrieved by calling <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage::Enum</a> on a particular item.

## -struct-fields

### -field propid

Type: <b>PROPID</b>

WIA property ID.

### -field pszName

Type: <b>LPOLESTR</b>

WIA property name. 

<div class="alert"><b>Note</b>  Property names are not localized. They are primarily used to support scripting languages; therefore, they are always the same on any system.</div>
<div> </div>