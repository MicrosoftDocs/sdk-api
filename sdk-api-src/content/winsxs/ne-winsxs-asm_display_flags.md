---
UID: NE:winsxs.__MIDL_IAssemblyName_0003
title: ASM_DISPLAY_FLAGS (winsxs.h)
description: The values of the ASM_DISPLAY_FLAGS enumeration are used by the GetDisplayName method to specify which portions of the assembly's full name to include in the string representation of the assembly name.
helpviewer_keywords: ["ASM_DISPLAYF_CULTURE","ASM_DISPLAYF_CUSTOM","ASM_DISPLAYF_LANGUAGEID","ASM_DISPLAYF_PROCESSORARCHITECTURE","ASM_DISPLAYF_PUBLIC_KEY","ASM_DISPLAYF_PUBLIC_KEY_TOKEN","ASM_DISPLAYF_VERSION","ASM_DISPLAY_FLAGS","ASM_DISPLAY_FLAGS","ASM_DISPLAY_FLAGS enumeration [Side-by-side Assemblies]","setup.asm_display_flags_","winsxs/ASM_DISPLAYF_CULTURE","winsxs/ASM_DISPLAYF_CUSTOM","winsxs/ASM_DISPLAYF_LANGUAGEID","winsxs/ASM_DISPLAYF_PROCESSORARCHITECTURE","winsxs/ASM_DISPLAYF_PUBLIC_KEY","winsxs/ASM_DISPLAYF_PUBLIC_KEY_TOKEN","winsxs/ASM_DISPLAYF_VERSION","winsxs/ASM_DISPLAY_FLAGS"]
old-location: setup\asm_display_flags_.htm
tech.root: setup
ms.assetid: 8f4c00b9-2684-44eb-9a68-bef6da87c396
ms.date: 12/05/2018
ms.keywords: ASM_DISPLAYF_CULTURE, ASM_DISPLAYF_CUSTOM, ASM_DISPLAYF_LANGUAGEID, ASM_DISPLAYF_PROCESSORARCHITECTURE, ASM_DISPLAYF_PUBLIC_KEY, ASM_DISPLAYF_PUBLIC_KEY_TOKEN, ASM_DISPLAYF_VERSION, ASM_DISPLAY_FLAGS, ASM_DISPLAY_FLAGS , ASM_DISPLAY_FLAGS enumeration [Side-by-side Assemblies], setup.asm_display_flags_, winsxs/ASM_DISPLAYF_CULTURE, winsxs/ASM_DISPLAYF_CUSTOM, winsxs/ASM_DISPLAYF_LANGUAGEID, winsxs/ASM_DISPLAYF_PROCESSORARCHITECTURE, winsxs/ASM_DISPLAYF_PUBLIC_KEY, winsxs/ASM_DISPLAYF_PUBLIC_KEY_TOKEN, winsxs/ASM_DISPLAYF_VERSION, winsxs/ASM_DISPLAY_FLAGS
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
req.typenames: ASM_DISPLAY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IAssemblyName_0003
 - winsxs/__MIDL_IAssemblyName_0003
 - ASM_DISPLAY_FLAGS
 - winsxs/ASM_DISPLAY_FLAGS
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
 - ASM_DISPLAY_FLAGS
---

# ASM_DISPLAY_FLAGS enumeration


## -description

The values of the  <b>ASM_DISPLAY_FLAGS</b> enumeration are used by the <a href="/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname">GetDisplayName</a> method to specify which portions of the assembly's full name to include in the string representation of the assembly name.

## -enum-fields

### -field ASM_DISPLAYF_VERSION:0x1

Include the version number.

### -field ASM_DISPLAYF_CULTURE:0x2

Include the culture.

### -field ASM_DISPLAYF_PUBLIC_KEY_TOKEN:0x4

Include the public key token.

### -field ASM_DISPLAYF_PUBLIC_KEY:0x8

Include the public key.

### -field ASM_DISPLAYF_CUSTOM:0x10

Include the custom part of the assembly name.

### -field ASM_DISPLAYF_PROCESSORARCHITECTURE:0x20

Include the processor architecture.

### -field ASM_DISPLAYF_LANGUAGEID:0x40

Reserved.
