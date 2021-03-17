---
UID: NF:shobjidl_core.FreeKnownFolderDefinitionFields
title: FreeKnownFolderDefinitionFields function (shobjidl_core.h)
description: Frees the allocated fields in the result from IKnownFolder::GetFolderDefinition.
helpviewer_keywords: ["FreeKnownFolderDefinitionFields","FreeKnownFolderDefinitionFields function [Windows Shell]","_shell_FreeKnownFolderDefinitionFields","shell.FreeKnownFolderDefinitionFields","shobjidl_core/FreeKnownFolderDefinitionFields"]
old-location: shell\FreeKnownFolderDefinitionFields.htm
tech.root: shell
ms.assetid: 0ad17dd3-e612-403a-b8c3-e93d5f259c1f
ms.date: 12/05/2018
ms.keywords: FreeKnownFolderDefinitionFields, FreeKnownFolderDefinitionFields function [Windows Shell], _shell_FreeKnownFolderDefinitionFields, shell.FreeKnownFolderDefinitionFields, shobjidl_core/FreeKnownFolderDefinitionFields
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeKnownFolderDefinitionFields
 - shobjidl_core/FreeKnownFolderDefinitionFields
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FreeKnownFolderDefinitionFields
---

# FreeKnownFolderDefinitionFields function


## -description

Frees the allocated fields in the result from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition">IKnownFolder::GetFolderDefinition</a>.

## -parameters

### -param pKFD [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a> structure that contains information about the given known folder.

## -remarks

This is an inline helper function that calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> on the fields in the structure that need to be freed. Its implementation can be seen in the header file.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>