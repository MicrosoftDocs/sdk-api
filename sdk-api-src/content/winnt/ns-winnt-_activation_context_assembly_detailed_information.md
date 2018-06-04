---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION structure


## -description


The 
<b>ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION</b> structure is used by the 
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> function.


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
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a>. For more information, see 
<a href="https://msdn.microsoft.com/0b78ecf6-fbff-4172-9b0d-09f993666db1">Assembly Versions</a>.


### -field ulManifestVersionMinor

Minor version of the assembly queried by 
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a>. For more information, see 
<a href="https://msdn.microsoft.com/0b78ecf6-fbff-4172-9b0d-09f993666db1">Assembly Versions</a>.


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
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> is called with the AssemblyDetailedInformationInActivationContext option, and the function succeeds, the information in the returned buffer is in the form of the 
<b>ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION</b> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION pAssemblyInfo = NULL;
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

if (GetCurrentActCtx(&amp;hActCtx)) {

    // Attempt to use our stack-based buffer first - if that's not large
    // enough, allocate from the heap and try again.
    fSuccess = QueryActCtxW(
        0, 
        hActCtx, 
        (PVOID)&amp;QueryIndex, 
        AssemblyDetailedInformationInActivationContext,
        pvDataBuffer,
        cbAvailable,
        &amp;cbRequired);

    // Failed, because the buffer was too small.
    if (!fSuccess &amp;&amp; (GetLastError() == ERROR_INSUFFICIENT_BUFFER)) {

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
            (PVOID)&amp;QueryIndex,
            AssemblyDetailedInformationInActivationContext,
            pvDataBuffer,
            cbAvailable,
            &amp;cbRequired);

    }

    if (fSuccess) {
        // Now that we've found the assembly info, cast our target buffer back to
        // the assembly info pointer.  Use pAssemblyInfo-&gt;lpFileName
        pAssemblyInfo = (PACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION)pvDataBuffer;
    }
}

DoneQuerying:
    if (hActCtx != INVALID_HANDLE_VALUE)
        ReleaseActCtx(hActCtx);

    if (pvDataBuffer &amp;&amp; (pvDataBuffer != bTemporaryBuffer)) {
        HeapFree(GetProcessHeap(), 0, pvDataBuffer);
        pvDataBuffer = 0;
    }
</pre>
</td>
</tr>
</table></span></div>


