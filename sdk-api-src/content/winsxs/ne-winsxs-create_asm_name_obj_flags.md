---
UID: NE:winsxs.__MIDL___MIDL_itf_winsxs_0000_0003_0001
title: CREATE_ASM_NAME_OBJ_FLAGS (winsxs.h)
description: The CREATE_ASM_NAME_OBJ_FLAGS enumeration is used by the CreateAssemblyNameObject function.
helpviewer_keywords: ["CANOF_PARSE_DISPLAY_NAME","CANOF_SET_DEFAULT_VALUES","CREATE_ASM_NAME_OBJ_FLAGS","CREATE_ASM_NAME_OBJ_FLAGS","CREATE_ASM_NAME_OBJ_FLAGS enumeration [Side-by-side Assemblies]","setup.create_asm_name_obj_flags_","winsxs/CANOF_PARSE_DISPLAY_NAME","winsxs/CANOF_SET_DEFAULT_VALUES","winsxs/CREATE_ASM_NAME_OBJ_FLAGS"]
old-location: setup\create_asm_name_obj_flags_.htm
tech.root: setup
ms.assetid: fdbb5eb0-0e45-483c-bcab-8b19a079800c
ms.date: 12/05/2018
ms.keywords: CANOF_PARSE_DISPLAY_NAME, CANOF_SET_DEFAULT_VALUES, CREATE_ASM_NAME_OBJ_FLAGS, CREATE_ASM_NAME_OBJ_FLAGS , CREATE_ASM_NAME_OBJ_FLAGS enumeration [Side-by-side Assemblies], setup.create_asm_name_obj_flags_, winsxs/CANOF_PARSE_DISPLAY_NAME, winsxs/CANOF_SET_DEFAULT_VALUES, winsxs/CREATE_ASM_NAME_OBJ_FLAGS
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
req.typenames: CREATE_ASM_NAME_OBJ_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsxs_0000_0003_0001
 - winsxs/__MIDL___MIDL_itf_winsxs_0000_0003_0001
 - CREATE_ASM_NAME_OBJ_FLAGS
 - winsxs/CREATE_ASM_NAME_OBJ_FLAGS
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
 - CREATE_ASM_NAME_OBJ_FLAGS
---

# CREATE_ASM_NAME_OBJ_FLAGS enumeration


## -description

The <b>CREATE_ASM_NAME_OBJ_FLAGS</b> enumeration is used by the <a href="/windows/desktop/api/winsxs/nf-winsxs-createassemblynameobject">CreateAssemblyNameObject</a> function.

If no  value is specified, the <i>szAssemblyName</i> parameter of the <a href="/windows/desktop/api/winsxs/nf-winsxs-createassemblynameobject">CreateAssemblyNameObject</a> function is the "Name" portion of the fully-specified assembly name.

## -enum-fields

### -field CANOF_PARSE_DISPLAY_NAME:0x1

If this flag is specified, the <i>szAssemblyName</i> parameter of <a href="/windows/desktop/api/winsxs/nf-winsxs-createassemblynameobject">CreateAssemblyNameObject</a> is a fully-specified side-by-side assembly name and is parsed to the individual properties.

### -field CANOF_SET_DEFAULT_VALUES:0x2

Reserved.
