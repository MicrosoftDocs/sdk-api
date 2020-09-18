---
UID: NS:winnt._ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
title: ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION (winnt.h)
description: The ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION structure is used by the QueryActCtxW function.
helpviewer_keywords: ["*PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION","ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION","ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION structure [Side-by-side Assemblies]","PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION","PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION structure pointer [Side-by-side Assemblies]","_ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION","_win32_activation_context_assembly_detailed_information","setup.activation_context_assembly_detailed_information","winnt/ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION","winnt/PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION"]
old-location: setup\activation_context_assembly_detailed_information.htm
tech.root: setup
ms.assetid: b093cc6a-55ea-49bf-904d-2b43517f9b02
ms.date: 12/05/2018
ms.keywords: '*PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION, ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION, ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION structure [Side-by-side Assemblies], PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION, PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION structure pointer [Side-by-side Assemblies], _ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION, _win32_activation_context_assembly_detailed_information, setup.activation_context_assembly_detailed_information, winnt/ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION, winnt/PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION'
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
req.typenames: ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION, *PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
 - winnt/_ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
 - PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
 - winnt/PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
 - ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
 - winnt/ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
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
 - ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION
---

# ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION structure


## -description

The 
<b>ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION</b> structure is used by the 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> function.

## -struct-fields

### -field ulFlags

This value is always 0.

### -field ulEncodedAssemblyIdentityLength

Length of the encoded assembly identity in bytes.

### -field ulManifestPathType

This value always a constant.

### -field ulManifestPathLength

Length of the assembly manifest path in bytes.

### -field liManifestLastWriteTime

The last time the manifest was written. This is in the form of a 
<b>FILETIME</b> data structure.

### -field ulPolicyPathType

This value always a constant.

### -field ulPolicyPathLength

Length of the publisher policy path in bytes.

### -field liPolicyLastWriteTime

The last time the policy was written. This is in the form of a 
<b>FILETIME</b> data structure.

### -field ulMetadataSatelliteRosterIndex

Metadata satellite roster index.

### -field ulManifestVersionMajor

Major version of the assembly queried by 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a>. For more information, see 
<a href="/windows/desktop/SbsCs/assembly-versions">Assembly Versions</a>.

### -field ulManifestVersionMinor

Minor version of the assembly queried by 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a>. For more information, see 
<a href="/windows/desktop/SbsCs/assembly-versions">Assembly Versions</a>.

### -field ulPolicyVersionMajor

Major version of any policy, if one exists.

### -field ulPolicyVersionMinor

Minor version of any policy, if one exists.

### -field ulAssemblyDirectoryNameLength

Length of the assembly directory name in bytes.

### -field lpAssemblyEncodedAssemblyIdentity

Pointer to a null-terminated string that contains a textually-encoded format of the assembly's identity.

### -field lpAssemblyManifestPath

Pointer to a null-terminated string that indicates the original path to this assembly's manifest.

### -field lpAssemblyPolicyPath

Pointer to a null-terminated string that indicates the path of whatever policy assembly was used to determine that this version of the assembly should be loaded. If this member is null, no policy was used to decide to load this version.

### -field lpAssemblyDirectoryName

Pointer to a null-terminated string that indicates the folder from which this assembly was loaded.

### -field ulFileCount

## -remarks

If 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> is called with the AssemblyDetailedInformationInActivationContext option, and the function succeeds, the information in the returned buffer is in the form of the 
<b>ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION</b> structure.


```cpp
PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION pAssemblyInfo = NULL;
ACTIVATION_CONTEXT_QUERY_INDEX QueryIndex;
BOOL fSuccess = FALSE;
SIZE_T cbRequired;
HANDLE hActCtx = INVALID_HANDLE_VALUE;
BYTE bTemporaryBuffer[512];
PVOID pvDataBuffer = (PVOID)bTemporaryBuffer;
SIZE_T cbAvailable = sizeof(bTemporaryBuffer);

// Request the first file in the root assembly
QueryIndex.ulAssemblyIndex = 1;
QueryIndex.ulFileIndexInAssembly = 0;

if (GetCurrentActCtx(&hActCtx)) {

    // Attempt to use our stack-based buffer first - if that's not large
    // enough, allocate from the heap and try again.
    fSuccess = QueryActCtxW(
        0, 
        hActCtx, 
        (PVOID)&QueryIndex, 
        AssemblyDetailedInformationInActivationContext,
        pvDataBuffer,
        cbAvailable,
        &cbRequired);

    // Failed, because the buffer was too small.
    if (!fSuccess && (GetLastError() == ERROR_INSUFFICIENT_BUFFER)) {

        // Allocate what we need from the heap - fail if there isn't enough
        // memory to do so.        
        pvDataBuffer = HeapAlloc(GetProcessHeap(), 0, cbRequired);
        if (pvDataBuffer == NULL) {
            fSuccess = FALSE;
            goto DoneQuerying;
        }
        cbAvailable = cbRequired;

        // If this fails again, exit out.
        fSuccess = QueryActCtxW(
            0, 
            hActCtx,
            (PVOID)&QueryIndex,
            AssemblyDetailedInformationInActivationContext,
            pvDataBuffer,
            cbAvailable,
            &cbRequired);

    }

    if (fSuccess) {
        // Now that we've found the assembly info, cast our target buffer back to
        // the assembly info pointer.  Use pAssemblyInfo->lpFileName
        pAssemblyInfo = (PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION)pvDataBuffer;
    }
}

DoneQuerying:
    if (hActCtx != INVALID_HANDLE_VALUE)
        ReleaseActCtx(hActCtx);

    if (pvDataBuffer && (pvDataBuffer != bTemporaryBuffer)) {
        HeapFree(GetProcessHeap(), 0, pvDataBuffer);
        pvDataBuffer = 0;
    }

```