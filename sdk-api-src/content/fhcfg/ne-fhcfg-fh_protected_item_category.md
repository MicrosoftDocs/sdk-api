---
UID: NE:fhcfg._FH_PROTECTED_ITEM_CATEGORY
title: FH_PROTECTED_ITEM_CATEGORY (fhcfg.h)
description: Specifies the type of an inclusion or exclusion list.
helpviewer_keywords: ["*PFH_PROTECTED_ITEM_CATEGORY","FH_FOLDER","FH_LIBRARY","FH_PROTECTED_ITEM_CATEGORY","FH_PROTECTED_ITEM_CATEGORY enumeration [Windows API]","MAX_PROTECTED_ITEM_CATEGORY","fhcfg/FH_FOLDER","fhcfg/FH_LIBRARY","fhcfg/FH_PROTECTED_ITEM_CATEGORY","fhcfg/MAX_PROTECTED_ITEM_CATEGORY","winprog.fh_protected_item_category"]
old-location: winprog\fh_protected_item_category.htm
tech.root: winprog
ms.assetid: 40AE4FB7-B81D-4CC1-B1A2-53952AE538DD
ms.date: 12/05/2018
ms.keywords: '*PFH_PROTECTED_ITEM_CATEGORY, FH_FOLDER, FH_LIBRARY, FH_PROTECTED_ITEM_CATEGORY, FH_PROTECTED_ITEM_CATEGORY enumeration [Windows API], MAX_PROTECTED_ITEM_CATEGORY, fhcfg/FH_FOLDER, fhcfg/FH_LIBRARY, fhcfg/FH_PROTECTED_ITEM_CATEGORY, fhcfg/MAX_PROTECTED_ITEM_CATEGORY, winprog.fh_protected_item_category'
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FH_PROTECTED_ITEM_CATEGORY, *PFH_PROTECTED_ITEM_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FH_PROTECTED_ITEM_CATEGORY
 - fhcfg/_FH_PROTECTED_ITEM_CATEGORY
 - PFH_PROTECTED_ITEM_CATEGORY
 - fhcfg/PFH_PROTECTED_ITEM_CATEGORY
 - FH_PROTECTED_ITEM_CATEGORY
 - fhcfg/FH_PROTECTED_ITEM_CATEGORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fhcfg.h
api_name:
 - FH_PROTECTED_ITEM_CATEGORY
---

# FH_PROTECTED_ITEM_CATEGORY enumeration


## -description

Specifies the type of an inclusion or exclusion list.

## -enum-fields

### -field FH_FOLDER:0

The inclusion or exclusion list is a list of folders.

### -field FH_LIBRARY

The inclusion or exclusion list is a list of libraries.

### -field MAX_PROTECTED_ITEM_CATEGORY

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.

## -remarks

To retrieve the inclusion and exclusion rules that are currently stored in an <a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object, call the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getincludeexcluderules">IFhConfigMgr::GetIncludeExcludeRules</a> method.

To add or remove an exclusion rule, call the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-addremoveexcluderule">IFhConfigMgr::AddRemoveExcludeRule</a> method.

## -see-also

<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-addremoveexcluderule">IFhConfigMgr::AddRemoveExcludeRule</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getincludeexcluderules">IFhConfigMgr::GetIncludeExcludeRules</a>
