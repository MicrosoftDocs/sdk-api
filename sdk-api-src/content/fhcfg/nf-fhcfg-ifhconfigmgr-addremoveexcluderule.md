---
UID: NF:fhcfg.IFhConfigMgr.AddRemoveExcludeRule
title: IFhConfigMgr::AddRemoveExcludeRule (fhcfg.h)
description: Adds an exclusion rule to the exclusion list or removes a rule from the list.
helpviewer_keywords: ["AddRemoveExcludeRule","AddRemoveExcludeRule method [Windows API]","AddRemoveExcludeRule method [Windows API]","FhConfigMgr class","AddRemoveExcludeRule method [Windows API]","IFhConfigMgr interface","FhConfigMgr class [Windows API]","AddRemoveExcludeRule method","IFhConfigMgr interface [Windows API]","AddRemoveExcludeRule method","IFhConfigMgr.AddRemoveExcludeRule","IFhConfigMgr::AddRemoveExcludeRule","fhcfg/IFhConfigMgr::AddRemoveExcludeRule","winprog.ifhconfigmgr_addremoveexcluderule"]
old-location: winprog\ifhconfigmgr_addremoveexcluderule.htm
tech.root: winprog
ms.assetid: 8900944D-3B73-49AB-AE26-F0B2D5842B02
ms.date: 12/05/2018
ms.keywords: AddRemoveExcludeRule, AddRemoveExcludeRule method [Windows API], AddRemoveExcludeRule method [Windows API],FhConfigMgr class, AddRemoveExcludeRule method [Windows API],IFhConfigMgr interface, FhConfigMgr class [Windows API],AddRemoveExcludeRule method, IFhConfigMgr interface [Windows API],AddRemoveExcludeRule method, IFhConfigMgr.AddRemoveExcludeRule, IFhConfigMgr::AddRemoveExcludeRule, fhcfg/IFhConfigMgr::AddRemoveExcludeRule, winprog.ifhconfigmgr_addremoveexcluderule
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
 - IFhConfigMgr::AddRemoveExcludeRule
 - fhcfg/IFhConfigMgr::AddRemoveExcludeRule
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
 - IFhConfigMgr.AddRemoveExcludeRule
 - FhConfigMgr.AddRemoveExcludeRule
---

# IFhConfigMgr::AddRemoveExcludeRule


## -description

Adds an exclusion rule to the exclusion list or removes a  rule from the list.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Add [in]

If this parameter is <b>TRUE</b>, a new exclusion rule is added.
If it is set to <b>FALSE</b>, an existing exclusion rule is removed.

### -param Category [in]

Specifies the type of the exclusion rule. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_protected_item_category">FH_PROTECTED_ITEM_CATEGORY</a> enumeration for possible values.

### -param Item [in]

The folder path or library name or GUID of the item that the exclusion rule applies to.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

The File History protection scope is the set of files that are backed up by the File History feature.  It contains inclusion rules and exclusion rules. Inclusion rules specify the files and folders that are included. Exclusion rules specify the files and folders that are excluded.

The default protection scope includes all folders from all user libraries and the  Contacts, Desktop, and Favorites folders.

Exclusion rules take precedence over inclusion rules. In other words, if an inclusion rule conflicts with an exclusion rule, the File History feature follows the exclusion rule.

To reduce the protection scope, use the <b>IFhConfigMgr::AddRemoveExcludeRule</b> to add exclusion rules. 

This method can be used to add or remove exclusion rules. It cannot be used to modify inclusion rules.

User libraries can be enumerated by calling the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem">SHGetKnownFolderItem</a> function and the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> interfaces.

Standard folders and libraries are specified by a GUID, prefixed with an asterisk. For example,  *a990ae9f-a03b-4e80-94bc-9912d7504104 specifies the Pictures library. For a list of standard folders and libraries and their GUIDs, see the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> documentation. 

Custom libraries are specified by name. Folders are specified by their full path (for example, C:\Users\Public\Videos).

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_protected_item_category">FH_PROTECTED_ITEM_CATEGORY</a>



<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getincludeexcluderules">IFhConfigMgr::GetIncludeExcludeRules</a>