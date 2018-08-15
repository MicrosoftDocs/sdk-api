---
UID: NE:winsxs.__MIDL___MIDL_itf_winsxs_0000_0003_0001
title: "__MIDL___MIDL_itf_winsxs_0000_0003_0001"
author: windows-sdk-content
description: The CREATE_ASM_NAME_OBJ_FLAGS enumeration is used by the CreateAssemblyNameObject function.
old-location: setup\create_asm_name_obj_flags_.htm
old-project: sbscs
ms.assetid: fdbb5eb0-0e45-483c-bcab-8b19a079800c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CANOF_PARSE_DISPLAY_NAME, CANOF_SET_DEFAULT_VALUES, CREATE_ASM_NAME_OBJ_FLAGS, CREATE_ASM_NAME_OBJ_FLAGS , CREATE_ASM_NAME_OBJ_FLAGS enumeration [Side-by-side Assemblies], __MIDL___MIDL_itf_winsxs_0000_0003_0001, setup.create_asm_name_obj_flags_, winsxs/CANOF_PARSE_DISPLAY_NAME, winsxs/CANOF_SET_DEFAULT_VALUES, winsxs/CREATE_ASM_NAME_OBJ_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winsxs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CREATE_ASM_NAME_OBJ_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsxs.h
api_name:
 - CREATE_ASM_NAME_OBJ_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# __MIDL___MIDL_itf_winsxs_0000_0003_0001 enumeration


## -description


The <b>CREATE_ASM_NAME_OBJ_FLAGS</b> enumeration is used by the <a href="https://msdn.microsoft.com/1290a0b3-28f9-46fb-a98f-40b43bc0df1a">CreateAssemblyNameObject</a> function.

If no  value is specified, the <i>szAssemblyName</i> parameter of the <a href="https://msdn.microsoft.com/1290a0b3-28f9-46fb-a98f-40b43bc0df1a">CreateAssemblyNameObject</a> function is the "Name" portion of the fully-specified assembly name.


## -enum-fields




### -field CANOF_PARSE_DISPLAY_NAME

If this flag is specified, the <i>szAssemblyName</i> parameter of <a href="https://msdn.microsoft.com/1290a0b3-28f9-46fb-a98f-40b43bc0df1a">CreateAssemblyNameObject</a> is a fully-specified side-by-side assembly name and is parsed to the individual properties.


### -field CANOF_SET_DEFAULT_VALUES

Reserved.

