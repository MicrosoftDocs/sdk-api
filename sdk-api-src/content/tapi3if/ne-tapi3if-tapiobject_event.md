---
UID: NE:tapi3if.TAPIOBJECT_EVENT
title: TAPIOBJECT_EVENT (tapi3if.h)
description: The TAPIOBJECT_EVENT enum describes TAPI object events. The ITTAPIObjectEvent::get_Event method returns a member of this enum to indicate the type of TAPI object event that occurred.
helpviewer_keywords: ["TAPIOBJECT_EVENT","TAPIOBJECT_EVENT enumeration [TAPI 2.2]","TE_ADDRESSCLOSE","TE_ADDRESSCREATE","TE_ADDRESSREMOVE","TE_REINIT","TE_TRANSLATECHANGE","_tapi3_tapiobject_event","tapi3.tapiobject_event","tapi3if/TAPIOBJECT_EVENT","tapi3if/TE_ADDRESSCLOSE","tapi3if/TE_ADDRESSCREATE","tapi3if/TE_ADDRESSREMOVE","tapi3if/TE_REINIT","tapi3if/TE_TRANSLATECHANGE"]
old-location: tapi3\tapiobject_event.htm
tech.root: tapi3
ms.assetid: 606e9f99-d90c-4d4a-8dd5-2734c9bd2e7e
ms.date: 12/05/2018
ms.keywords: TAPIOBJECT_EVENT, TAPIOBJECT_EVENT enumeration [TAPI 2.2], TE_ADDRESSCLOSE, TE_ADDRESSCREATE, TE_ADDRESSREMOVE, TE_REINIT, TE_TRANSLATECHANGE, _tapi3_tapiobject_event, tapi3.tapiobject_event, tapi3if/TAPIOBJECT_EVENT, tapi3if/TE_ADDRESSCLOSE, tapi3if/TE_ADDRESSCREATE, tapi3if/TE_ADDRESSREMOVE, tapi3if/TE_REINIT, tapi3if/TE_TRANSLATECHANGE
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TAPIOBJECT_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TAPIOBJECT_EVENT
 - tapi3if/TAPIOBJECT_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TAPIOBJECT_EVENT
---

# TAPIOBJECT_EVENT enumeration


## -description

The 
<b>TAPIOBJECT_EVENT</b> enum describes TAPI object events. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapiobjectevent-get_event">ITTAPIObjectEvent::get_Event</a> method returns a member of this enum to indicate the type of TAPI object event that occurred.

## -enum-fields

### -field TE_ADDRESSCREATE:0

A new address has been created.

### -field TE_ADDRESSREMOVE

An address has been moved.

### -field TE_REINIT

The TAPI object has been reinitialized

### -field TE_TRANSLATECHANGE

A translation change has occurred.

### -field TE_ADDRESSCLOSE

Address has been closed.

### -field TE_PHONECREATE

### -field TE_PHONEREMOVE

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapiobjectevent-get_event">ITTAPIObjectEvent::get_Event</a>
