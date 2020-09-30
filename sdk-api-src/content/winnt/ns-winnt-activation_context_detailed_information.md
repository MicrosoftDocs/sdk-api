---
UID: NS:winnt._ACTIVATION_CONTEXT_DETAILED_INFORMATION
title: ACTIVATION_CONTEXT_DETAILED_INFORMATION (winnt.h)
description: The ACTIVATION_CONTEXT_DETAILED_INFORMATION structure is used by the QueryActCtxW function.
helpviewer_keywords: ["*PACTIVATION_CONTEXT_DETAILED_INFORMATION","ACTIVATION_CONTEXT_DETAILED_INFORMATION","ACTIVATION_CONTEXT_DETAILED_INFORMATION structure [Side-by-side Assemblies]","PACTIVATION_CONTEXT_DETAILED_INFORMATION","PACTIVATION_CONTEXT_DETAILED_INFORMATION structure pointer [Side-by-side Assemblies]","_ACTIVATION_CONTEXT_DETAILED_INFORMATION","_win32_activation_context_detailed_information","setup.activation_context_detailed_information","winnt/ACTIVATION_CONTEXT_DETAILED_INFORMATION","winnt/PACTIVATION_CONTEXT_DETAILED_INFORMATION"]
old-location: setup\activation_context_detailed_information.htm
tech.root: setup
ms.assetid: 58e4acfe-d5c8-45ae-bf32-469229ffc836
ms.date: 12/05/2018
ms.keywords: '*PACTIVATION_CONTEXT_DETAILED_INFORMATION, ACTIVATION_CONTEXT_DETAILED_INFORMATION, ACTIVATION_CONTEXT_DETAILED_INFORMATION structure [Side-by-side Assemblies], PACTIVATION_CONTEXT_DETAILED_INFORMATION, PACTIVATION_CONTEXT_DETAILED_INFORMATION structure pointer [Side-by-side Assemblies], _ACTIVATION_CONTEXT_DETAILED_INFORMATION, _win32_activation_context_detailed_information, setup.activation_context_detailed_information, winnt/ACTIVATION_CONTEXT_DETAILED_INFORMATION, winnt/PACTIVATION_CONTEXT_DETAILED_INFORMATION'
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
req.typenames: ACTIVATION_CONTEXT_DETAILED_INFORMATION, *PACTIVATION_CONTEXT_DETAILED_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTIVATION_CONTEXT_DETAILED_INFORMATION
 - winnt/_ACTIVATION_CONTEXT_DETAILED_INFORMATION
 - PACTIVATION_CONTEXT_DETAILED_INFORMATION
 - winnt/PACTIVATION_CONTEXT_DETAILED_INFORMATION
 - ACTIVATION_CONTEXT_DETAILED_INFORMATION
 - winnt/ACTIVATION_CONTEXT_DETAILED_INFORMATION
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
 - ACTIVATION_CONTEXT_DETAILED_INFORMATION
---

# ACTIVATION_CONTEXT_DETAILED_INFORMATION structure


## -description

The 
<b>ACTIVATION_CONTEXT_DETAILED_INFORMATION</b> structure is used by the 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> function.

## -struct-fields

### -field dwFlags

This value is always 0.

### -field ulFormatVersion

This value specifies the format of the returned information. On WindowsÂ XP and WindowsÂ Server 2003 this member is always 1.

### -field ulAssemblyCount

Number of assemblies in the activation context.

### -field ulRootManifestPathType

Specifies the kind of path from which this assembly's manifest was loaded. 

This member is always one of the following constants:

### -field ulRootManifestPathChars

Number of characters in the manifest path.

### -field ulRootConfigurationPathType

Specifies the kind of path from which this assembly's application configuration manifest was loaded. 

This member is always one of the following constants:

### -field ulRootConfigurationPathChars

Number of characters in any application configuration file path.

### -field ulAppDirPathType

Specifies the kind of path from which this application manifest was loaded. 

This member is always one of the following constants:

### -field ulAppDirPathChars

Number of characters in the application directory.

### -field lpRootManifestPath

Path of the application manifest.

### -field lpRootConfigurationPath

Path of the configuration file.

### -field lpAppDirPath

Path of the application directory.

## -remarks

If 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> is called with the ActivationContextDetailedInformation option, and the function succeeds, the information in the returned buffer is in the form of the 
<b>ACTIVATION_CONTEXT_DETAILED_INFORMATION</b> structure. The following is an example of a structure used to hold detailed information about the activation context and a call from 
<b>QueryActCtxW</b>.


```cpp
PACTIVATION_CONTEXT_DETAILED_INFORMATION pAssemblyInfo = NULL;
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
        pAssemblyInfo = (PACTIVATION_CONTEXT_DETAILED_INFORMATION)pvDataBuffer;
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