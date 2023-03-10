---
UID: NS:iads._ADS_CASEIGNORE_LIST
title: ADS_CASEIGNORE_LIST (iads.h)
description: The ADS_CASEIGNORE_LIST structure is an ADSI representation of the Case Ignore List attribute syntax.
helpviewer_keywords: ["*PADS_CASEIGNORE_LIST","ADS_CASEIGNORE_LIST","ADS_CASEIGNORE_LIST structure [ADSI]","PADS_CASEIGNORE_LIST","PADS_CASEIGNORE_LIST structure pointer [ADSI]","_ds_ads_caseignore_list","adsi.ads__caseignore__list","adsi.ads_caseignore_list","iads/ADS_CASEIGNORE_LIST","iads/PADS_CASEIGNORE_LIST"]
old-location: adsi\ads_caseignore_list.htm
tech.root: adsi
ms.assetid: 448c4541-7478-44f3-9be3-f1200f83978a
ms.date: 12/05/2018
ms.keywords: '*PADS_CASEIGNORE_LIST, ADS_CASEIGNORE_LIST, ADS_CASEIGNORE_LIST structure [ADSI], PADS_CASEIGNORE_LIST, PADS_CASEIGNORE_LIST structure pointer [ADSI], _ds_ads_caseignore_list, adsi.ads__caseignore__list, adsi.ads_caseignore_list, iads/ADS_CASEIGNORE_LIST, iads/PADS_CASEIGNORE_LIST'
req.header: iads.h
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
req.typenames: ADS_CASEIGNORE_LIST, *PADS_CASEIGNORE_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ADS_CASEIGNORE_LIST
 - iads/_ADS_CASEIGNORE_LIST
 - PADS_CASEIGNORE_LIST
 - iads/PADS_CASEIGNORE_LIST
 - ADS_CASEIGNORE_LIST
 - iads/ADS_CASEIGNORE_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_CASEIGNORE_LIST
---

# ADS_CASEIGNORE_LIST structure


## -description

The <b>ADS_CASEIGNORE_LIST</b> structure is an ADSI representation of the <b>Case Ignore List</b> attribute syntax.

## -struct-fields

### -field Next

Pointer to the next <b>ADS_CASEIGNORE_LIST</b> in the list of case-insensitive strings.

### -field String

The null-terminated Unicode string value of the current entry of the list.

## -remarks

A <b>Case Ignore List</b> attribute represents an ordered sequence of case insensitive strings.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>