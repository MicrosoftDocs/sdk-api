---
UID: NS:winbase.tagACTCTX_SECTION_KEYED_DATA
title: ACTCTX_SECTION_KEYED_DATA (winbase.h)
description: The ACTCTX_SECTION_KEYED_DATA structure is used by the FindActCtxSectionString and FindActCtxSectionGuid functions to return the activation context information along with either the GUID or 32-bit integer-tagged activation context section.
helpviewer_keywords: ["*PACTCTX_SECTION_KEYED_DATA","ACTCTX_SECTION_KEYED_DATA","ACTCTX_SECTION_KEYED_DATA structure [Side-by-side Assemblies]","PACTCTX_SECTION_KEYED_DATA","PACTCTX_SECTION_KEYED_DATA structure pointer [Side-by-side Assemblies]","_win32_actctx_section_keyed_data_str","setup.actctx_section_keyed_data_str","tagACTCTX_SECTION_KEYED_DATA","winbase/ACTCTX_SECTION_KEYED_DATA","winbase/PACTCTX_SECTION_KEYED_DATA"]
old-location: setup\actctx_section_keyed_data_str.htm
tech.root: setup
ms.assetid: c73160e7-fff5-4ba5-8b3a-895ac944c76d
ms.date: 12/05/2018
ms.keywords: '*PACTCTX_SECTION_KEYED_DATA, ACTCTX_SECTION_KEYED_DATA, ACTCTX_SECTION_KEYED_DATA structure [Side-by-side Assemblies], PACTCTX_SECTION_KEYED_DATA, PACTCTX_SECTION_KEYED_DATA structure pointer [Side-by-side Assemblies], _win32_actctx_section_keyed_data_str, setup.actctx_section_keyed_data_str, tagACTCTX_SECTION_KEYED_DATA, winbase/ACTCTX_SECTION_KEYED_DATA, winbase/PACTCTX_SECTION_KEYED_DATA'
req.header: winbase.h
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
req.typenames: ACTCTX_SECTION_KEYED_DATA, *PACTCTX_SECTION_KEYED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagACTCTX_SECTION_KEYED_DATA
 - winbase/tagACTCTX_SECTION_KEYED_DATA
 - PACTCTX_SECTION_KEYED_DATA
 - winbase/PACTCTX_SECTION_KEYED_DATA
 - ACTCTX_SECTION_KEYED_DATA
 - winbase/ACTCTX_SECTION_KEYED_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - ACTCTX_SECTION_KEYED_DATA
---

# ACTCTX_SECTION_KEYED_DATA structure


## -description

The 
<b>ACTCTX_SECTION_KEYED_DATA</b> structure is used by the 
<a href="/windows/desktop/api/winbase/nf-winbase-findactctxsectionstringa">FindActCtxSectionString</a> and 
<a href="/windows/desktop/api/winbase/nf-winbase-findactctxsectionguid">FindActCtxSectionGuid</a> functions to return the activation context information along with either the GUID or 32-bit integer-tagged activation context section.

## -struct-fields

### -field cbSize

The size, in bytes, of the activation context keyed data structure.

### -field ulDataFormatVersion

Number that indicates the format of the data in the section where the key was found. Clients should verify that the data format version is as expected rather than trying to interpret the values of unfamiliar data formats. This number is only changed when major non-backward-compatible changes to the section data formats need to be made. The current format version is 1.

### -field lpData

Pointer to the redirection data found associated with the section identifier and key.

### -field ulLength

Number of bytes in the structure referred to by <b>lpData</b>. Note that the data structures  grow over time; do not access members in the instance data that extend beyond <b>ulLength</b>.

### -field lpSectionGlobalData

Returned pointer to a section-specific data structure which is global to the activation context section where the key was found. Its interpretation depends on the section identifier requested.

### -field ulSectionGlobalDataLength

Number of bytes in the section global data block referred to by <b>lpSectionGlobalData</b>. 




Note that the data structures  grow over time and you may receive an old format activation context data block; do not access members in the section global data that extend beyond <b>ulSectionGlobalDataLength</b>.

### -field lpSectionBase

Pointer to the base of the section where the key was found. Some instance data contains offsets relative to the section base address, in which case this pointer value is used.

### -field ulSectionTotalLength

Number of bytes for the entire section starting at <b>lpSectionBase</b>. May be used to verify that offset/length pairs, which are specified as relative to the section base are wholly contained in the section.

### -field hActCtx

Handle to the activation context where the key was found. First, the active activation context for the thread is searched, followed by the process-default activation context and then the system-compatible-default-activation context. This member indicates which activation context contained the section and key requested. This is only returned if the FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX flag is passed. 




Note that when this is returned, the caller must call 
<a href="/windows/desktop/api/winbase/nf-winbase-releaseactctx">ReleaseActCtx</a>() on the activation context handle returned to release system resources when all other references to the activation context have been released.

### -field ulAssemblyRosterIndex

Cardinal number of the assembly in the activation context that provided the redirection information found. This value can be presented to <a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> for more information about the contributing assembly.

### -field ulFlags

### -field AssemblyMetadata

## -remarks

Callers should initialize the 
<b>ACTCTX_SECTION_KEYED_DATA</b> structure as such:

"ACTCTX_SECTION_KEYED_DATA askd = { sizeof(askd) };"

which  initializes all members to zero/null except the size field which is set correctly.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findactctxsectionguid">FindActCtxSectionGuid</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findactctxsectionstringa">FindActCtxSectionString</a>