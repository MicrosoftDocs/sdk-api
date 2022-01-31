---
UID: NE:cscobj.tagOFFLINEFILES_COMPARE
title: OFFLINEFILES_COMPARE (cscobj.h)
description: Specifies the type of comparison to perform in the IOfflineFilesItemFilter::GetTimeFilter method.
helpviewer_keywords: ["OFFLINEFILES_COMPARE","OFFLINEFILES_COMPARE enumeration [Offline Files]","OFFLINEFILES_COMPARE_EQ","OFFLINEFILES_COMPARE_GT","OFFLINEFILES_COMPARE_GTE","OFFLINEFILES_COMPARE_LT","OFFLINEFILES_COMPARE_LTE","OFFLINEFILES_COMPARE_NEQ","cscobj/OFFLINEFILES_COMPARE","cscobj/OFFLINEFILES_COMPARE_EQ","cscobj/OFFLINEFILES_COMPARE_GT","cscobj/OFFLINEFILES_COMPARE_GTE","cscobj/OFFLINEFILES_COMPARE_LT","cscobj/OFFLINEFILES_COMPARE_LTE","cscobj/OFFLINEFILES_COMPARE_NEQ","of.offlinefiles_compare"]
old-location: of\offlinefiles_compare.htm
tech.root: of
ms.assetid: 17972c96-4ce1-43c0-bb6d-730787f0f93a
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_COMPARE, OFFLINEFILES_COMPARE enumeration [Offline Files], OFFLINEFILES_COMPARE_EQ, OFFLINEFILES_COMPARE_GT, OFFLINEFILES_COMPARE_GTE, OFFLINEFILES_COMPARE_LT, OFFLINEFILES_COMPARE_LTE, OFFLINEFILES_COMPARE_NEQ, cscobj/OFFLINEFILES_COMPARE, cscobj/OFFLINEFILES_COMPARE_EQ, cscobj/OFFLINEFILES_COMPARE_GT, cscobj/OFFLINEFILES_COMPARE_GTE, cscobj/OFFLINEFILES_COMPARE_LT, cscobj/OFFLINEFILES_COMPARE_LTE, cscobj/OFFLINEFILES_COMPARE_NEQ, of.offlinefiles_compare
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_COMPARE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_COMPARE
 - cscobj/tagOFFLINEFILES_COMPARE
 - OFFLINEFILES_COMPARE
 - cscobj/OFFLINEFILES_COMPARE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_COMPARE
---

# OFFLINEFILES_COMPARE enumeration


## -description

Specifies the type of comparison to perform in the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemfilter-gettimefilter">IOfflineFilesItemFilter::GetTimeFilter</a> method.

## -enum-fields

### -field OFFLINEFILES_COMPARE_EQ:0

Check whether the item value is equal to the filter value.

### -field OFFLINEFILES_COMPARE_NEQ

Check whether the item value is not equal to the filter value.

### -field OFFLINEFILES_COMPARE_LT

Check whether the item value is less than the filter value.

### -field OFFLINEFILES_COMPARE_GT

Check whether the item value is greater than the filter value.

### -field OFFLINEFILES_COMPARE_LTE

Check whether the item value is less than or equal to the filter value.

### -field OFFLINEFILES_COMPARE_GTE

Check whether the item value is greater than or equal to the filter value.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemfilter-gettimefilter">IOfflineFilesItemFilter::GetTimeFilter</a>
