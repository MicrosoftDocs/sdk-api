---
UID: NS:winnt._ACTIVATION_CONTEXT_QUERY_INDEX
title: ACTIVATION_CONTEXT_QUERY_INDEX (winnt.h)
description: The ACTIVATION_CONTEXT_QUERY_INDEX structure is used by QueryActCtxW function.
helpviewer_keywords: ["*PACTIVATION_CONTEXT_QUERY_INDEX","ACTIVATION_CONTEXT_QUERY_INDEX","ACTIVATION_CONTEXT_QUERY_INDEX structure [Side-by-side Assemblies]","PACTIVATION_CONTEXT_QUERY_INDEX","PACTIVATION_CONTEXT_QUERY_INDEX structure pointer [Side-by-side Assemblies]","_ACTIVATION_CONTEXT_QUERY_INDEX","_win32_activation_context_query_index","setup.activation_context_query_index","winnt/ACTIVATION_CONTEXT_QUERY_INDEX","winnt/PACTIVATION_CONTEXT_QUERY_INDEX"]
old-location: setup\activation_context_query_index.htm
tech.root: SbsCs
ms.assetid: eb15895c-07c9-4b68-83ef-2f2b8e3b271c
ms.date: 12/05/2018
ms.keywords: '*PACTIVATION_CONTEXT_QUERY_INDEX, ACTIVATION_CONTEXT_QUERY_INDEX, ACTIVATION_CONTEXT_QUERY_INDEX structure [Side-by-side Assemblies], PACTIVATION_CONTEXT_QUERY_INDEX, PACTIVATION_CONTEXT_QUERY_INDEX structure pointer [Side-by-side Assemblies], _ACTIVATION_CONTEXT_QUERY_INDEX, _win32_activation_context_query_index, setup.activation_context_query_index, winnt/ACTIVATION_CONTEXT_QUERY_INDEX, winnt/PACTIVATION_CONTEXT_QUERY_INDEX'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: ACTIVATION_CONTEXT_QUERY_INDEX, *PACTIVATION_CONTEXT_QUERY_INDEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTIVATION_CONTEXT_QUERY_INDEX
 - winnt/_ACTIVATION_CONTEXT_QUERY_INDEX
 - PACTIVATION_CONTEXT_QUERY_INDEX
 - winnt/PACTIVATION_CONTEXT_QUERY_INDEX
 - ACTIVATION_CONTEXT_QUERY_INDEX
 - winnt/ACTIVATION_CONTEXT_QUERY_INDEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACTIVATION_CONTEXT_QUERY_INDEX
---

# ACTIVATION_CONTEXT_QUERY_INDEX structure


## -description

The 
<b>ACTIVATION_CONTEXT_QUERY_INDEX</b> structure is used by 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> function.

## -struct-fields

### -field ulAssemblyIndex

One-based index of the assembly whose file table is to be queried.

### -field ulFileIndexInAssembly

Zero-based index of the file in the above assembly to be queried.

## -remarks

Calling the 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> function with the FileInformationInAssemblyOfAssemblyInActivationContext option requires that the <i>pvSubInstance</i> parameter point to an 
<b>ACTIVATION_CONTEXT_QUERY_INDEX</b> structure. See the sample for 
<a href="/windows/desktop/api/winnt/ns-winnt-assembly_file_detailed_information">ASSEMBLY_FILE_DETAILED_INFORMATION</a> for an example of its use.