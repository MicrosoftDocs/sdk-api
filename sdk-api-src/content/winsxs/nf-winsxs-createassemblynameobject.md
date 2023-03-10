---
UID: NF:winsxs.CreateAssemblyNameObject
title: CreateAssemblyNameObject function (winsxs.h)
description: The CreateAssemblyNameObject function obtains an instance of the IAssemblyName interface.
helpviewer_keywords: ["CreateAssemblyNameObject","CreateAssemblyNameObject function [Side-by-side Assemblies]","setup.createassemblynameobject","winsxs/CreateAssemblyNameObject"]
old-location: setup\createassemblynameobject.htm
tech.root: setup
ms.assetid: 1290a0b3-28f9-46fb-a98f-40b43bc0df1a
ms.date: 12/05/2018
ms.keywords: CreateAssemblyNameObject, CreateAssemblyNameObject function [Side-by-side Assemblies], setup.createassemblynameobject, winsxs/CreateAssemblyNameObject
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
req.dll: Sxs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateAssemblyNameObject
 - winsxs/CreateAssemblyNameObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - sxs.dll
api_name:
 - CreateAssemblyNameObject
---

# CreateAssemblyNameObject function


## -description

The <b>CreateAssemblyNameObject</b> function obtains an instance of the <a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a> interface.

## -parameters

### -param ppAssemblyNameObj

Pointer to a location that receives the <a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblyname">IAssemblyName</a> pointer.

### -param szAssemblyName

A pointer to a string value containing  the name of a side-by-side assembly. Depending on  <i>dwFlags</i>, this is a string representation of the fully-specified side-by-side assembly name or the Name portion of the assembly   name. The string value can be <b>NULL</b>.

### -param dwFlags

The value of this parameter can be a combination of <a href="/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags">CREATE_ASM_NAME_OBJ_FLAGS</a> enumeration options or 0. If the value is <b>CANOF_PARSE_DISPLAY_NAME</b>, the <i>szAssemblyName</i> parameter contains a string representation of the fully-specified side-by-side assembly name and is parsed to the individual properties. If 0, <i>szAssemblyName</i> is the Name portion of the side-by-side assembly name.

### -param pvReserved

This parameter is reserved and must be <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.