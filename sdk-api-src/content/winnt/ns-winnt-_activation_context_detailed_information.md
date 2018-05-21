---
UID: NS:winnt._ACTIVATION_CONTEXT_DETAILED_INFORMATION
title: "_ACTIVATION_CONTEXT_DETAILED_INFORMATION"
author: windows-driver-content
description: The ACTIVATION_CONTEXT_DETAILED_INFORMATION structure is used by the QueryActCtxW function.
old-location: setup\activation_context_detailed_information.htm
old-project: SbsCs
ms.assetid: 58e4acfe-d5c8-45ae-bf32-469229ffc836
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PACTIVATION_CONTEXT_DETAILED_INFORMATION, ACTIVATION_CONTEXT_DETAILED_INFORMATION, ACTIVATION_CONTEXT_DETAILED_INFORMATION structure [Side-by-side Assemblies], PACTIVATION_CONTEXT_DETAILED_INFORMATION, PACTIVATION_CONTEXT_DETAILED_INFORMATION structure pointer [Side-by-side Assemblies], _ACTIVATION_CONTEXT_DETAILED_INFORMATION, _win32_activation_context_detailed_information, setup.activation_context_detailed_information, winnt/ACTIVATION_CONTEXT_DETAILED_INFORMATION, winnt/PACTIVATION_CONTEXT_DETAILED_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: ACTIVATION_CONTEXT_DETAILED_INFORMATION, *PACTIVATION_CONTEXT_DETAILED_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	ACTIVATION_CONTEXT_DETAILED_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ACTIVATION_CONTEXT_DETAILED_INFORMATION structure


## -description


The 
<b>ACTIVATION_CONTEXT_DETAILED_INFORMATION</b> structure is used by the 
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> function.


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
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> is called with the ActivationContextDetailedInformation option, and the function succeeds, the information in the returned buffer is in the form of the 
<b>ACTIVATION_CONTEXT_DETAILED_INFORMATION</b> structure. The following is an example of a structure used to hold detailed information about the activation context and a call from 
<b>QueryActCtxW</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PACTIVATION_CONTEXT_DETAILED_INFORMATION pAssemblyInfo = NULL;
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
        pAssemblyInfo = (PACTIVATION_CONTEXT_DETAILED_INFORMATION)pvDataBuffer;
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


