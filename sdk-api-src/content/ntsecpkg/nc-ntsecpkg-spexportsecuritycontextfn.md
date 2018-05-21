---
UID: NC:ntsecpkg.SpExportSecurityContextFn
title: SpExportSecurityContextFn
author: windows-driver-content
description: Exports a security context to another process.
old-location: security\spexportsecuritycontext.htm
old-project: SecAuthN
ms.assetid: 0c8cafb3-aaf5-4937-91dc-e534bb6e4caf
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: SECPKG_CONTEXT_EXPORT_DELETE_OLD, SECPKG_CONTEXT_EXPORT_RESET_NEW, SpExportSecurityContext, SpExportSecurityContext function [Security], SpExportSecurityContextFn, _ssp_spexportsecuritycontext, ntsecpkg/SpExportSecurityContext, security.spexportsecuritycontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	SpExportSecurityContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SpExportSecurityContextFn callback function


## -description


Exports a security context to another process.

The <b>SpExportSecurityContext</b> function is the dispatch function for the 
<a href="https://msdn.microsoft.com/4ebc7f37-b948-4c78-973f-0a74e55c7ee2">ExportSecurityContext</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param phContext [in]

A handle to the security context to export.


### -param fFlags [in]

Optional. Specifies context duplication options. The following table lists the valid values which are defined in Sspi.h. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CONTEXT_EXPORT_RESET_NEW"></a><a id="secpkg_context_export_reset_new"></a><dl>
<dt><b>SECPKG_CONTEXT_EXPORT_RESET_NEW</b></dt>
</dl>
</td>
<td width="60%">
New context is reset to initial state.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CONTEXT_EXPORT_DELETE_OLD"></a><a id="secpkg_context_export_delete_old"></a><dl>
<dt><b>SECPKG_CONTEXT_EXPORT_DELETE_OLD</b></dt>
</dl>
</td>
<td width="60%">
Old context is deleted during export.

</td>
</tr>
</table>
 


### -param pPackedContext [out]

Pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure containing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">serialized</a> context. Resources should be allocated using the 
<a href="https://msdn.microsoft.com/2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe">AllocateClientBuffer</a> function, and freed by the caller using the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.


### -param pToken [out]

Optional. Pointer to a handle that receives the context's token.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



To import a previously exported security context use the 
<a href="https://msdn.microsoft.com/f3a9427b-37f0-464a-9f67-3b4e09597a98">SpImportSecurityContext</a> function.

SSP/APs must implement the <b>SpExportSecurityContext</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpExportSecurityContext</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/f3a9427b-37f0-464a-9f67-3b4e09597a98">SpImportSecurityContext</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

