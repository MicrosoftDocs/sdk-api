---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL_IAssemblyName_0001 enumeration


## -description


The values of the <b>ASM_NAME</b> enumeration are the property IDs for the name-value pairs included in a  side-by-side assembly name.


## -enum-fields




### -field ASM_NAME_PUBLIC_KEY

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

