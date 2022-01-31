---
UID: NE:wuapi.tagUpdateType
title: UpdateType (wuapi.h)
description: Defines the types of update, such as a driver or software update.
helpviewer_keywords: ["UpdateType","UpdateType enumeration [Windows Update Agent]","utDriver","utSoftware","wua.updatetype","wuapi/UpdateType","wuapi/utDriver","wuapi/utSoftware"]
old-location: wua\updatetype.htm
tech.root: wua
ms.assetid: 2845075f-f27a-44f5-8dc3-bdf67ce15c79
ms.date: 12/05/2018
ms.keywords: UpdateType, UpdateType enumeration [Windows Update Agent], utDriver, utSoftware, wua.updatetype, wuapi/UpdateType, wuapi/utDriver, wuapi/utSoftware
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UpdateType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateType
 - wuapi/tagUpdateType
 - UpdateType
 - wuapi/UpdateType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateType
---

# UpdateType enumeration


## -description

Defines the types of update, such as a driver or software update.

## -enum-fields

### -field utSoftware:1

Indicates that the update is a software update.

### -field utDriver:2

Indicates that the update is a driver update.

## -see-also

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_type">IUpdate.Type</a>
