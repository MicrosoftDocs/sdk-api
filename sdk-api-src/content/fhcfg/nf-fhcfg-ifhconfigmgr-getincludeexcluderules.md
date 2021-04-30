---
UID: NF:fhcfg.IFhConfigMgr.GetIncludeExcludeRules
title: IFhConfigMgr::GetIncludeExcludeRules (fhcfg.h)
description: Retrieves the inclusion and exclusion rules that are currently stored in an FhConfigMgr object.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","GetIncludeExcludeRules method","GetIncludeExcludeRules","GetIncludeExcludeRules method [Windows API]","GetIncludeExcludeRules method [Windows API]","FhConfigMgr class","GetIncludeExcludeRules method [Windows API]","IFhConfigMgr interface","IFhConfigMgr interface [Windows API]","GetIncludeExcludeRules method","IFhConfigMgr.GetIncludeExcludeRules","IFhConfigMgr::GetIncludeExcludeRules","fhcfg/IFhConfigMgr::GetIncludeExcludeRules","winprog.ifhconfigmgr_getincludeexcluderules"]
old-location: winprog\ifhconfigmgr_getincludeexcluderules.htm
tech.root: winprog
ms.assetid: DE137C08-923D-4ADC-8EBC-2F277F72CAE4
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],GetIncludeExcludeRules method, GetIncludeExcludeRules, GetIncludeExcludeRules method [Windows API], GetIncludeExcludeRules method [Windows API],FhConfigMgr class, GetIncludeExcludeRules method [Windows API],IFhConfigMgr interface, IFhConfigMgr interface [Windows API],GetIncludeExcludeRules method, IFhConfigMgr.GetIncludeExcludeRules, IFhConfigMgr::GetIncludeExcludeRules, fhcfg/IFhConfigMgr::GetIncludeExcludeRules, winprog.ifhconfigmgr_getincludeexcluderules
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFhConfigMgr::GetIncludeExcludeRules
 - fhcfg/IFhConfigMgr::GetIncludeExcludeRules
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.GetIncludeExcludeRules
 - FhConfigMgr.GetIncludeExcludeRules
---

# IFhConfigMgr::GetIncludeExcludeRules


## -description

Retrieves the inclusion and exclusion rules that are currently stored in an <a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Include [in]

If set to <b>TRUE</b>, inclusion rules are returned. If set to <b>FALSE</b>, exclusion rules are returned.

### -param Category [in]

An <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_protected_item_category">FH_PROTECTED_ITEM_CATEGORY</a> enumeration value that specifies the type of the inclusion or exclusion rules.

### -param Iterator [out]

Receives an <a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhscopeiterator">IFhScopeIterator</a> interface pointer that can be used to enumerate the rules in the requested category.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

The File History protection scope is the set of files that are backed up by this feature.  It contains inclusion rules and exclusion rules. Inclusion rules specify the files and folders that are included. Exclusion rules specify the files and folders that are excluded.

The default protection scope includes all folders from all user libraries and the  Contacts, Desktop, and Favorites folders.

You can modify the File History protection scope  by adding exclusion rules to reduce the File History protection scope without removing folders from user libraries.

Exclusion rules take precedence over inclusion rules. In other words, if an inclusion rule conflicts with an exclusion rule, the File History feature follows the exclusion rule.

The <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-addremoveexcluderule">IFhConfigMgr::AddRemoveExcludeRule</a> method can be used to add or remove exclusion rules. It cannot be used to modify the inclusion rules.

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_protected_item_category">FH_PROTECTED_ITEM_CATEGORY</a>



<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-addremoveexcluderule">IFhConfigMgr::AddRemoveExcludeRule</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhscopeiterator">IFhScopeIterator</a>