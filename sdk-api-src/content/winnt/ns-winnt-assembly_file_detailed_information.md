---
UID: NS:winnt._ASSEMBLY_FILE_DETAILED_INFORMATION
title: ASSEMBLY_FILE_DETAILED_INFORMATION (winnt.h)
description: The ASSEMBLY_FILE_DETAILED_INFORMATION structure is used by the QueryActCtxW function.
helpviewer_keywords: ["*PASSEMBLY_FILE_DETAILED_INFORMATION","ASSEMBLY_FILE_DETAILED_INFORMATION","ASSEMBLY_FILE_DETAILED_INFORMATION structure [Side-by-side Assemblies]","PASSEMBLY_FILE_DETAILED_INFORMATION","PASSEMBLY_FILE_DETAILED_INFORMATION structure pointer [Side-by-side Assemblies]","_ASSEMBLY_FILE_DETAILED_INFORMATION","_win32_assembly_file_detailed_information","setup.assembly_file_detailed_information","winnt/ASSEMBLY_FILE_DETAILED_INFORMATION","winnt/PASSEMBLY_FILE_DETAILED_INFORMATION"]
old-location: setup\assembly_file_detailed_information.htm
tech.root: setup
ms.assetid: 7f1e5155-a6c1-4b6a-be47-37fab337186c
ms.date: 12/05/2018
ms.keywords: '*PASSEMBLY_FILE_DETAILED_INFORMATION, ASSEMBLY_FILE_DETAILED_INFORMATION, ASSEMBLY_FILE_DETAILED_INFORMATION structure [Side-by-side Assemblies], PASSEMBLY_FILE_DETAILED_INFORMATION, PASSEMBLY_FILE_DETAILED_INFORMATION structure pointer [Side-by-side Assemblies], _ASSEMBLY_FILE_DETAILED_INFORMATION, _win32_assembly_file_detailed_information, setup.assembly_file_detailed_information, winnt/ASSEMBLY_FILE_DETAILED_INFORMATION, winnt/PASSEMBLY_FILE_DETAILED_INFORMATION'
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
req.typenames: ASSEMBLY_FILE_DETAILED_INFORMATION, *PASSEMBLY_FILE_DETAILED_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ASSEMBLY_FILE_DETAILED_INFORMATION
 - winnt/_ASSEMBLY_FILE_DETAILED_INFORMATION
 - PASSEMBLY_FILE_DETAILED_INFORMATION
 - winnt/PASSEMBLY_FILE_DETAILED_INFORMATION
 - ASSEMBLY_FILE_DETAILED_INFORMATION
 - winnt/ASSEMBLY_FILE_DETAILED_INFORMATION
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
 - ASSEMBLY_FILE_DETAILED_INFORMATION
---

# ASSEMBLY_FILE_DETAILED_INFORMATION structure


## -description

The 
<b>ASSEMBLY_FILE_DETAILED_INFORMATION</b> structure is used by the 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> function.

## -struct-fields

### -field ulFlags

This value is always 0.

### -field ulFilenameLength

Length in bytes of the file name pointed to by <b>lpFileName</b>. The count does not include the terminating null character.

### -field ulPathLength

Length in bytes of the path string pointed to by <b>lpFilePath</b> The count does not include the terminating null character.

### -field lpFileName

Null-terminated string that specifies the name of the file.

### -field lpFilePath

Null-terminated string that specifies the path to the file named in <b>lpFileName</b>.

## -remarks

If 
<a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> is called with the FileInformationInAssemblyOfAssemblyInActivationContext option, and the function succeeds, the information in the returned buffer is in form of the 
<b>ASSEMBLY_FILE_DETAILED_INFORMATION</b> structure. The following is an example of a structure used to hold detailed information about the activation context and a call from 
<b>QueryActCtxW</b>.


```cpp
PASSEMBLY_FILE_DETAILED_INFORMATION pAssemblyInfo = NULL;
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
        FileInformationInAssemblyOfAssemblyInActivationContext,
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
            FileInformationInAssemblyOfAssemblyInActivationContext,
            pvDataBuffer,
            cbAvailable,
            &cbRequired);

    }

    if (fSuccess) {
        // Now that we've found the assembly info, cast our target buffer back to
        // the assembly info pointer.  Use pAssemblyInfo->lpFileName
        pAssemblyInfo = (PASSEMBLY_FILE_DETAILED_INFORMATION)pvDataBuffer;
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