---
UID: NE:fhcfg._FH_PROTECTED_ITEM_CATEGORY
title: "_FH_PROTECTED_ITEM_CATEGORY"
author: windows-sdk-content
description: Specifies the type of an inclusion or exclusion list.
old-location: winprog\fh_protected_item_category.htm
old-project: devnotes
ms.assetid: 40AE4FB7-B81D-4CC1-B1A2-53952AE538DD
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PFH_PROTECTED_ITEM_CATEGORY, FH_FOLDER, FH_LIBRARY, FH_PROTECTED_ITEM_CATEGORY, FH_PROTECTED_ITEM_CATEGORY enumeration [Windows API], MAX_PROTECTED_ITEM_CATEGORY, _FH_PROTECTED_ITEM_CATEGORY, fhcfg/FH_FOLDER, fhcfg/FH_LIBRARY, fhcfg/FH_PROTECTED_ITEM_CATEGORY, fhcfg/MAX_PROTECTED_ITEM_CATEGORY, winprog.fh_protected_item_category"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fhcfg.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FH_PROTECTED_ITEM_CATEGORY, *PFH_PROTECTED_ITEM_CATEGORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fhcfg.h
api_name:
 - FH_PROTECTED_ITEM_CATEGORY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# _FH_PROTECTED_ITEM_CATEGORY enumeration


## -description


Specifies the type of an inclusion or exclusion list.


## -enum-fields




### -field FH_FOLDER

The inclusion or exclusion list is a list of folders.


### -field FH_LIBRARY

The inclusion or exclusion list is a list of libraries.


### -field MAX_PROTECTED_ITEM_CATEGORY

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.


## -remarks



To retrieve the inclusion and exclusion rules that are currently stored in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object, call the <a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a> method.

To add or remove an exclusion rule, call the <a href="https://msdn.microsoft.com/8900944D-3B73-49AB-AE26-F0B2D5842B02">IFhConfigMgr::AddRemoveExcludeRule</a> method.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/8900944D-3B73-49AB-AE26-F0B2D5842B02">IFhConfigMgr::AddRemoveExcludeRule</a>



<a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a>
 

 

