---
UID: NF:winbase.FindActCtxSectionGuid
title: FindActCtxSectionGuid function
author: windows-sdk-content
description: The FindActCtxSectionGuid function retrieves information on a specific GUID in the current activation context and returns a ACTCTX_SECTION_KEYED_DATA structure.
old-location: setup\findactctxsectionguid.htm
old-project: sbscs
ms.assetid: 3889505c-29a0-49dd-aca8-a26417b25a94
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX, FindActCtxSectionGuid, FindActCtxSectionGuid function [Side-by-side Assemblies], _win32_findactctxsectionguid, setup.findactctxsectionguid, winbase/FindActCtxSectionGuid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-sidebyside-l1-1-0.dll
 - KernelBase.dll
api_name:
 - FindActCtxSectionGuid
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindActCtxSectionGuid function


## -description


The 
<b>FindActCtxSectionGuid</b> function retrieves information on a specific GUID in the current activation context and returns a 
<a href="https://msdn.microsoft.com/c73160e7-fff5-4ba5-8b3a-895ac944c76d">ACTCTX_SECTION_KEYED_DATA</a> structure.


## -parameters




### -param dwFlags [in]

Flags that determine how this function is to operate. Only the following flag is currently defined. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX"></a><a id="find_actctx_section_key_return_hactctx"></a><dl>
<dt><b>FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX</b></dt>
</dl>
</td>
<td width="60%">
This function returns the activation context handle where the redirection data was found in the <b>hActCtx</b> member of the 
<a href="https://msdn.microsoft.com/c73160e7-fff5-4ba5-8b3a-895ac944c76d">ACTCTX_SECTION_KEYED_DATA</a> structure. The caller must use 
<a href="https://msdn.microsoft.com/aaf58969-06b7-4981-83af-651252339186">ReleaseActCtx</a> to release this activation context.

</td>
</tr>
</table>
 


### -param lpExtensionGuid [in]

Reserved; must be null.


### -param ulSectionId [in]

Identifier of the section of the activation context in which to search for the specified GUID. 




The following are valid GUID section identifiers:

<ul>
<li>ACTIVATION_CONTEXT_SECTION_COM_SERVER_REDIRECTION</li>
<li>ACTIVATION_CONTEXT_SECTION_COM_INTERFACE_REDIRECTION</li>
<li>ACTIVATION_CONTEXT_SECTION_COM_TYPE_LIBRARY_REDIRECTION</li>
</ul>
The following is a valid GUID section identifier beginning with Windows Server 2003 and Windows XP with SP1:

<ul>
<li>ACTIVATION_CONTEXT_SECTION_CLR_SURROGATES</li>
</ul>

### -param lpGuidToFind [in]

Pointer to a GUID to be used as the search criteria.


### -param ReturnedData [out]

Pointer to an 
<a href="https://msdn.microsoft.com/c73160e7-fff5-4ba5-8b3a-895ac944c76d">ACTCTX_SECTION_KEYED_DATA</a> structure to be filled out with the requested GUID information.


## -returns



If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



This function should only be called by the Side-by-side API functions or COM methods. Applications should not directly call this function.




## -see-also




<a href="https://msdn.microsoft.com/c73160e7-fff5-4ba5-8b3a-895ac944c76d">ACTCTX_SECTION_KEYED_DATA</a>



<a href="https://msdn.microsoft.com/d3f0b057-44ec-47ec-a0aa-69f3540b8900">FindActCtxSectionString</a>
 

 

