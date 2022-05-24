---
UID: NE:deliveryoptimization._DODownloadCostPolicy
tech.root: delivery_optimization
title: DODownloadCostPolicy
ms.date: 05/04/2022
targetos: Windows
description: Specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: deliveryoptimization.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - deliveryoptimization.h
api_name:
 - _DODownloadCostPolicy
 - DODownloadCostPolicy
f1_keywords:
 - _DODownloadCostPolicy
 - deliveryoptimization/_DODownloadCostPolicy
 - DODownloadCostPolicy
 - deliveryoptimization/DODownloadCostPolicy
dev_langs:
 - c++
helpviewer_keywords:
 - _DODownloadCostPolicy
prerelease: false
---

## -description

The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.

## -enum-fields

### -field DODownloadCostPolicy_Always

Download runs regardless of the cost.

### -field DODownloadCostPolicy_Unrestricted

Download runs unless imposes costs or traffic limits.

### -field DODownloadCostPolicy_Standard

Download runs unless neither subject to a surcharge nor near exhaustion.

### -field DODownloadCostPolicy_NoRoaming

Download runs unless that connectivity is subject to roaming surcharges.

### -field DODownloadCostPolicy_NoSurcharge

Download runs unless subject to a surcharge.

### -field DODownloadCostPolicy_NoCellular

Download runs unless network is on cellular.

## -remarks

## -see-also
