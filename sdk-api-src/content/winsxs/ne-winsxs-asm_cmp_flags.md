---
UID: NE:winsxs.__MIDL_IAssemblyName_0004
title: ASM_CMP_FLAGS (winsxs.h)
author: windows-sdk-content
description: The values of the ASM_CMP_FLAGS enumeration are used by the IsEqual method to specify which portions of two assembly names to compare.
old-location: setup\asm_cmp_flags_.htm
tech.root: SbsCs
ms.assetid: 3dd1ac40-e729-409d-a109-8e4f5fd12b37
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ASM_CMPF_ALL, ASM_CMPF_BUILD_NUMBER, ASM_CMPF_CULTURE, ASM_CMPF_CUSTOM, ASM_CMPF_DEFAULT, ASM_CMPF_MAJOR_VERSION, ASM_CMPF_MINOR_VERSION, ASM_CMPF_NAME, ASM_CMPF_PUBLIC_KEY_TOKEN, ASM_CMPF_REVISION_NUMBER, ASM_CMP_FLAGS, ASM_CMP_FLAGS , ASM_CMP_FLAGS enumeration [Side-by-side Assemblies], setup.asm_cmp_flags_, winsxs/ASM_CMPF_ALL, winsxs/ASM_CMPF_BUILD_NUMBER, winsxs/ASM_CMPF_CULTURE, winsxs/ASM_CMPF_CUSTOM, winsxs/ASM_CMPF_DEFAULT, winsxs/ASM_CMPF_MAJOR_VERSION, winsxs/ASM_CMPF_MINOR_VERSION, winsxs/ASM_CMPF_NAME, winsxs/ASM_CMPF_PUBLIC_KEY_TOKEN, winsxs/ASM_CMPF_REVISION_NUMBER, winsxs/ASM_CMP_FLAGS
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsxs.h
api_name:
 - ASM_CMP_FLAGS
product: Windows
targetos: Windows
req.typenames: ASM_CMP_FLAGS
req.redist: 
ms.custom: 19H1
---

# ASM_CMP_FLAGS enumeration


## -description


The values of the <b>ASM_CMP_FLAGS</b> enumeration are used by the <a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal">IsEqual</a> method to specify which portions of two assembly names to compare.


## -enum-fields




### -field ASM_CMPF_NAME

Compare the name portion of the assembly names.


### -field ASM_CMPF_MAJOR_VERSION

Compare the major version portion of the assembly names.


### -field ASM_CMPF_MINOR_VERSION

Compare the minor version portion of the assembly names.


### -field ASM_CMPF_BUILD_NUMBER

Compare the build version portion of the assembly names.


### -field ASM_CMPF_REVISION_NUMBER

Compare the revision version portion of the assembly names.


### -field ASM_CMPF_PUBLIC_KEY_TOKEN

Compare the public key token portion of the assembly names.


### -field ASM_CMPF_CULTURE

Compare the culture portion of the assembly names.


### -field ASM_CMPF_CUSTOM

Compare the custom portion of the assembly names.


### -field ASM_CMPF_ALL

Compare all portions of the assembly names. This is equivalent to setting:

ASM_CMPF_NAME | ASM_CMPF_MAJOR_VERSION | ASM_CMPF_MINOR_VERSION | ASM_CMPF_REVISION_NUMBER | ASM_CMPF_BUILD_NUMBER | ASM_CMPF_PUBLIC_KEY_TOKEN | ASM_CMPF_CULTURE | ASM_CMPF_CUSTOM


### -field ASM_CMPF_DEFAULT

 Ignore the version number to compare assemblies with simple names.

