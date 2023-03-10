---
UID: NE:winsxs.__MIDL_IAssemblyName_0001
title: ASM_NAME (winsxs.h)
description: The values of the ASM_NAME enumeration are the property IDs for the name-value pairs included in a side-by-side assembly name.
helpviewer_keywords: ["ASM_NAME","ASM_NAME","ASM_NAME enumeration [Side-by-side Assemblies]","ASM_NAME_ALIAS","ASM_NAME_BUILD_NUMBER","ASM_NAME_CODEBASE_LASTMOD","ASM_NAME_CODEBASE_URL","ASM_NAME_CULTURE","ASM_NAME_CUSTOM","ASM_NAME_HASH_ALGID","ASM_NAME_HASH_VALUE","ASM_NAME_MAJOR_VERSION","ASM_NAME_MAX_PARAMS","ASM_NAME_MINOR_VERSION","ASM_NAME_MVID","ASM_NAME_NAME","ASM_NAME_NULL_CUSTOM","ASM_NAME_NULL_PUBLIC_KEY","ASM_NAME_NULL_PUBLIC_KEY_TOKEN","ASM_NAME_OSINFO_ARRAY","ASM_NAME_PROCESSOR_ID_ARRAY","ASM_NAME_PUBLIC_KEY","ASM_NAME_PUBLIC_KEY_TOKEN","ASM_NAME_REVISION_NUMBER","setup.asm_name_","winsxs/ASM_NAME","winsxs/ASM_NAME_ALIAS","winsxs/ASM_NAME_BUILD_NUMBER","winsxs/ASM_NAME_CODEBASE_LASTMOD","winsxs/ASM_NAME_CODEBASE_URL","winsxs/ASM_NAME_CULTURE","winsxs/ASM_NAME_CUSTOM","winsxs/ASM_NAME_HASH_ALGID","winsxs/ASM_NAME_HASH_VALUE","winsxs/ASM_NAME_MAJOR_VERSION","winsxs/ASM_NAME_MAX_PARAMS","winsxs/ASM_NAME_MINOR_VERSION","winsxs/ASM_NAME_MVID","winsxs/ASM_NAME_NAME","winsxs/ASM_NAME_NULL_CUSTOM","winsxs/ASM_NAME_NULL_PUBLIC_KEY","winsxs/ASM_NAME_NULL_PUBLIC_KEY_TOKEN","winsxs/ASM_NAME_OSINFO_ARRAY","winsxs/ASM_NAME_PROCESSOR_ID_ARRAY","winsxs/ASM_NAME_PUBLIC_KEY","winsxs/ASM_NAME_PUBLIC_KEY_TOKEN","winsxs/ASM_NAME_REVISION_NUMBER"]
old-location: setup\asm_name_.htm
tech.root: setup
ms.assetid: 5e13e90e-68b0-4842-97de-4f179d4c9ad7
ms.date: 12/05/2018
ms.keywords: ASM_NAME, ASM_NAME , ASM_NAME enumeration [Side-by-side Assemblies], ASM_NAME_ALIAS, ASM_NAME_BUILD_NUMBER, ASM_NAME_CODEBASE_LASTMOD, ASM_NAME_CODEBASE_URL, ASM_NAME_CULTURE, ASM_NAME_CUSTOM, ASM_NAME_HASH_ALGID, ASM_NAME_HASH_VALUE, ASM_NAME_MAJOR_VERSION, ASM_NAME_MAX_PARAMS, ASM_NAME_MINOR_VERSION, ASM_NAME_MVID, ASM_NAME_NAME, ASM_NAME_NULL_CUSTOM, ASM_NAME_NULL_PUBLIC_KEY, ASM_NAME_NULL_PUBLIC_KEY_TOKEN, ASM_NAME_OSINFO_ARRAY, ASM_NAME_PROCESSOR_ID_ARRAY, ASM_NAME_PUBLIC_KEY, ASM_NAME_PUBLIC_KEY_TOKEN, ASM_NAME_REVISION_NUMBER, setup.asm_name_, winsxs/ASM_NAME, winsxs/ASM_NAME_ALIAS, winsxs/ASM_NAME_BUILD_NUMBER, winsxs/ASM_NAME_CODEBASE_LASTMOD, winsxs/ASM_NAME_CODEBASE_URL, winsxs/ASM_NAME_CULTURE, winsxs/ASM_NAME_CUSTOM, winsxs/ASM_NAME_HASH_ALGID, winsxs/ASM_NAME_HASH_VALUE, winsxs/ASM_NAME_MAJOR_VERSION, winsxs/ASM_NAME_MAX_PARAMS, winsxs/ASM_NAME_MINOR_VERSION, winsxs/ASM_NAME_MVID, winsxs/ASM_NAME_NAME, winsxs/ASM_NAME_NULL_CUSTOM, winsxs/ASM_NAME_NULL_PUBLIC_KEY, winsxs/ASM_NAME_NULL_PUBLIC_KEY_TOKEN, winsxs/ASM_NAME_OSINFO_ARRAY, winsxs/ASM_NAME_PROCESSOR_ID_ARRAY, winsxs/ASM_NAME_PUBLIC_KEY, winsxs/ASM_NAME_PUBLIC_KEY_TOKEN, winsxs/ASM_NAME_REVISION_NUMBER
req.header: winsxs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ASM_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IAssemblyName_0001
 - winsxs/__MIDL_IAssemblyName_0001
 - ASM_NAME
 - winsxs/ASM_NAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsxs.h
api_name:
 - ASM_NAME
---

# ASM_NAME enumeration


## -description

The values of the <b>ASM_NAME</b> enumeration are the property IDs for the name-value pairs included in a  side-by-side assembly name.

## -enum-fields

### -field ASM_NAME_PUBLIC_KEY:0

Property ID for the assembly's public key. The value is a byte array.

### -field ASM_NAME_PUBLIC_KEY_TOKEN

Property ID for the assembly's public key token. The value is a byte array.

### -field ASM_NAME_HASH_VALUE

Property ID for a reserved name-value pair. The value is a byte array.

### -field ASM_NAME_NAME

Property ID for the assembly's simple name.  The value is a string value.

### -field ASM_NAME_MAJOR_VERSION

Property ID for the assembly's major version.  The value is a <b>WORD</b> value.

### -field ASM_NAME_MINOR_VERSION

Property ID for the assembly's minor version. The value is a <b>WORD</b> value.

### -field ASM_NAME_BUILD_NUMBER

 Property ID for the assembly's build version.  The value  is a <b>WORD</b> value.

### -field ASM_NAME_REVISION_NUMBER

 Property ID for the assembly's revision version.   The value is a <b>WORD</b> value.

### -field ASM_NAME_CULTURE

 Property ID for the assembly's culture. The value is a string value.

### -field ASM_NAME_PROCESSOR_ID_ARRAY

Property ID for a reserved name-value pair.

### -field ASM_NAME_OSINFO_ARRAY

Property ID for a reserved name-value pair.

### -field ASM_NAME_HASH_ALGID

Property ID for a reserved name-value pair.    The value is a <b>DWORD</b> value.

### -field ASM_NAME_ALIAS

Property ID for a reserved name-value pair.

### -field ASM_NAME_CODEBASE_URL

Property ID for a reserved name-value pair.

### -field ASM_NAME_CODEBASE_LASTMOD

Property ID for a reserved name-value pair.    The value is a <b>FILETIME</b> structure.

### -field ASM_NAME_NULL_PUBLIC_KEY

Property ID for the assembly as a simply named assembly that does not have a public key.

### -field ASM_NAME_NULL_PUBLIC_KEY_TOKEN

Property ID for the assembly as a simply named assembly that does not have a public key token.

### -field ASM_NAME_CUSTOM

Property ID for a reserved name-value pair.        The value is a string value.

### -field ASM_NAME_NULL_CUSTOM

Property ID for a reserved name-value pair.

### -field ASM_NAME_MVID

Property ID for a reserved name-value pair.

### -field ASM_NAME_MAX_PARAMS

Reserved.

