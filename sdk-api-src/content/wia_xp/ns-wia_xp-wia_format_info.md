---
UID: NS:wia_xp._WIA_FORMAT_INFO
title: WIA_FORMAT_INFO (wia_xp.h)
description: The WIA_FORMAT_INFO structure specifies valid format and media type pairs for a device.
helpviewer_keywords: ["*PWIA_FORMAT_INFO","PWIA_FORMAT_INFO","PWIA_FORMAT_INFO structure pointer [WIA]","WIA_FORMAT_INFO","WIA_FORMAT_INFO structure [WIA]","_wia_WIA_FORMAT_INFO","wia._wia_WIA_FORMAT_INFO","wia_xp/PWIA_FORMAT_INFO","wia_xp/WIA_FORMAT_INFO"]
old-location: wia\_wia_WIA_FORMAT_INFO.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_format_info.htm
ms.date: 12/05/2018
ms.keywords: '*PWIA_FORMAT_INFO, PWIA_FORMAT_INFO, PWIA_FORMAT_INFO structure pointer [WIA], WIA_FORMAT_INFO, WIA_FORMAT_INFO structure [WIA], _wia_WIA_FORMAT_INFO, wia._wia_WIA_FORMAT_INFO, wia_xp/PWIA_FORMAT_INFO, wia_xp/WIA_FORMAT_INFO'
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
req.typenames: WIA_FORMAT_INFO, *PWIA_FORMAT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIA_FORMAT_INFO
 - wia_xp/_WIA_FORMAT_INFO
 - PWIA_FORMAT_INFO
 - wia_xp/PWIA_FORMAT_INFO
 - WIA_FORMAT_INFO
 - wia_xp/WIA_FORMAT_INFO
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
 - WIA_FORMAT_INFO
archived: true
---

# WIA_FORMAT_INFO structure


## -description

The <b>WIA_FORMAT_INFO</b> structure specifies valid format and media type pairs for a device.

## -struct-fields

### -field guidFormatID

Type: <b>GUID</b>

GUID that identifies the format.

### -field lTymed

Type: <b>LONG</b>

The media type that corresponds to the <b>guidFormatID</b> member.

