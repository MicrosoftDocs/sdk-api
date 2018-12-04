---
UID: NF:fhcfg.IFhConfigMgr.GetIncludeExcludeRules
title: IFhConfigMgr::GetIncludeExcludeRules
author: windows-sdk-content
description: Retrieves the inclusion and exclusion rules that are currently stored in an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_getincludeexcluderules.htm
tech.root: devnotes
ms.assetid: DE137C08-923D-4ADC-8EBC-2F277F72CAE4
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: FhConfigMgr class [Windows API],GetIncludeExcludeRules method, GetIncludeExcludeRules, GetIncludeExcludeRules method [Windows API], GetIncludeExcludeRules method [Windows API],FhConfigMgr class, GetIncludeExcludeRules method [Windows API],IFhConfigMgr interface, IFhConfigMgr interface [Windows API],GetIncludeExcludeRules method, IFhConfigMgr.GetIncludeExcludeRules, IFhConfigMgr::GetIncludeExcludeRules, fhcfg/IFhConfigMgr::GetIncludeExcludeRules, winprog.ifhconfigmgr_getincludeexcluderules
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFhConfigMgr::GetIncludeExcludeRules


## -description


Retrieves the inclusion and exclusion rules that are currently stored in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.


## -parameters




### -param Include [in]

If set to <b>TRUE</b>, inclusion rules are returned. If set to <b>FALSE</b>, exclusion rules are returned.


### -param Category [in]

An <a href="https://msdn.microsoft.com/40AE4FB7-B81D-4CC1-B1A2-53952AE538DD">FH_PROTECTED_ITEM_CATEGORY</a> enumeration value that specifies the type of the inclusion or exclusion rules.


### -param Iterator [out]

Receives an <a href="https://msdn.microsoft.com/E8F993BD-CB53-474A-926D-AED0F5A17073">IFhScopeIterator</a> interface pointer that can be used to enumerate the rules in the requested category.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



The File History protection scope is the set of files that are backed up by this feature.  It contains inclusion rules and exclusion rules. Inclusion rules specify the files and folders that are included. Exclusion rules specify the files and folders that are excluded.

The default protection scope includes all folders from all user libraries and the  Contacts, Desktop, and Favorites folders.

You can modify the File History protection scope  by adding exclusion rules to reduce the File History protection scope without removing folders from user libraries.

Exclusion rules take precedence over inclusion rules. In other words, if an inclusion rule conflicts with an exclusion rule, the File History feature follows the exclusion rule.

The <a href="https://msdn.microsoft.com/8900944D-3B73-49AB-AE26-F0B2D5842B02">IFhConfigMgr::AddRemoveExcludeRule</a> method can be used to add or remove exclusion rules. It cannot be used to modify the inclusion rules.




## -see-also




<a href="https://msdn.microsoft.com/40AE4FB7-B81D-4CC1-B1A2-53952AE538DD">FH_PROTECTED_ITEM_CATEGORY</a>



<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/8900944D-3B73-49AB-AE26-F0B2D5842B02">IFhConfigMgr::AddRemoveExcludeRule</a>



<a href="https://msdn.microsoft.com/E8F993BD-CB53-474A-926D-AED0F5A17073">IFhScopeIterator</a>
 

 

