---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0002
title: WcmNamespaceEnumerationFlags (wcmconfig.h)
description: Describes the types of enumeration flags.
helpviewer_keywords: ["AllEnumeration","SharedEnumeration","UserEnumeration","WcmNamespaceEnumerationFlags","WcmNamespaceEnumerationFlags enumeration [SMI]","smi.wcmnamespaceenumerationflags","wcmconfig/AllEnumeration","wcmconfig/SharedEnumeration","wcmconfig/UserEnumeration","wcmconfig/WcmNamespaceEnumerationFlags"]
old-location: smi\wcmnamespaceenumerationflags.htm
tech.root: SMI
ms.assetid: 606fad95-1f93-4e16-9be5-2ebd52b91180
ms.date: 12/05/2018
ms.keywords: AllEnumeration, SharedEnumeration, UserEnumeration, WcmNamespaceEnumerationFlags, WcmNamespaceEnumerationFlags enumeration [SMI], smi.wcmnamespaceenumerationflags, wcmconfig/AllEnumeration, wcmconfig/SharedEnumeration, wcmconfig/UserEnumeration, wcmconfig/WcmNamespaceEnumerationFlags
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WcmNamespaceEnumerationFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wcmconfig_0000_0000_0002
 - wcmconfig/__MIDL___MIDL_itf_wcmconfig_0000_0000_0002
 - WcmNamespaceEnumerationFlags
 - wcmconfig/WcmNamespaceEnumerationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmNamespaceEnumerationFlags
---

# WcmNamespaceEnumerationFlags enumeration


## -description

Describes the types of enumeration flags.

## -enum-fields

### -field SharedEnumeration:1

Describes a shared enumeration. It enumerates all namespaces that have been compiled for the machine space.

### -field UserEnumeration:2

Describes a user-specific  enumeration. It enumerates the namespaces that have been compiled for a specific user.

### -field AllEnumeration

A logical "OR" of shared and user enumeration.

## -remarks

<div class="alert"><b>Note</b>  UserEnumeration should not be used. No namespaces are compiled for a particular user, they are all compiled for the machine as an entity.</div>
<div> </div>

