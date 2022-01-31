---
UID: NE:bdaiface.SmartCardStatusType
title: SmartCardStatusType (bdaiface.h)
description: The SmartCardStatusType enumeration type specifies the status of a smart card.
helpviewer_keywords: ["CardDataChanged","CardError","CardFirmwareUpgrade","CardInserted","CardRemoved","SmartCardStatusType","SmartCardStatusType enumeration [Microsoft TV Technologies]","bdaiface/CardDataChanged","bdaiface/CardError","bdaiface/CardFirmwareUpgrade","bdaiface/CardInserted","bdaiface/CardRemoved","bdaiface/SmartCardStatusType","mstv.smartcardstatustype"]
old-location: mstv\smartcardstatustype.htm
tech.root: mstv
ms.assetid: c699c6a9-f554-4e2d-ac7f-9b5ff954fa6b
ms.date: 12/05/2018
ms.keywords: CardDataChanged, CardError, CardFirmwareUpgrade, CardInserted, CardRemoved, SmartCardStatusType, SmartCardStatusType enumeration [Microsoft TV Technologies], bdaiface/CardDataChanged, bdaiface/CardError, bdaiface/CardFirmwareUpgrade, bdaiface/CardInserted, bdaiface/CardRemoved, bdaiface/SmartCardStatusType, mstv.smartcardstatustype
req.header: bdaiface.h
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
req.typenames: SmartCardStatusType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SmartCardStatusType
 - bdaiface/SmartCardStatusType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bdaiface.h
api_name:
 - SmartCardStatusType
---

# SmartCardStatusType enumeration


## -description

The <b>SmartCardStatusType</b> enumeration type specifies the status of a smart card.

## -enum-fields

### -field CardInserted:0

The card was inserted.

### -field CardRemoved

The card was removed.

### -field CardError

An error occurred.

### -field CardDataChanged

The card data has changed.

### -field CardFirmwareUpgrade

Firmware upgrade.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-types">BDA Enumeration Types</a>
