---
UID: NS:lpmapi.IS_ADSPEC_BODY
title: IS_ADSPEC_BODY (lpmapi.h)
description: The IS_ADSPEC_BODY structure contains Integrated Services Adspec information.
helpviewer_keywords: ["IS_ADSPEC_BODY","IS_ADSPEC_BODY structure [QOS]","lpmapi/IS_ADSPEC_BODY","qos.is_adspec_body"]
old-location: qos\is_adspec_body.htm
tech.root: QOS
ms.assetid: f788e094-0b50-4104-be15-3593f53120c5
ms.date: 12/05/2018
ms.keywords: IS_ADSPEC_BODY, IS_ADSPEC_BODY structure [QOS], lpmapi/IS_ADSPEC_BODY, qos.is_adspec_body
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IS_ADSPEC_BODY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IS_ADSPEC_BODY
 - lpmapi/IS_ADSPEC_BODY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - IS_ADSPEC_BODY
---

# IS_ADSPEC_BODY structure


## -description

The 
<b>IS_ADSPEC_BODY</b> structure contains Integrated Services Adspec information.

## -struct-fields

### -field adspec_mh

Main header information and length, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservmainhdr">IntServMainHdr</a> structure.

### -field adspec_genparms

General Adspec parameter fragment, followed by variable-length fragments for some or all services.

## -remarks

The variable-length fragments that follow the <b>adspec_genparams</b> member can be minimal length fragments.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservmainhdr">IntServMainHdr</a>

