---
UID: NS:winnt._ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION
title: ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION (winnt.h)
author: windows-sdk-content
description: The ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION structure is used by the QueryActCtxW function.
old-location: setup\activation_context_compatibility_information.htm
tech.root: SbsCs
ms.assetid: d8c1ef4a-8e64-45bd-a185-b4af7932a0d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION, ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION, ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION structure [Setup API], PACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION, PACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION structure pointer [Setup API], _ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION, setup.activation_context_compatibility_information, winnt/ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION, winnt/PACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION"
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION
product: Windows
targetos: Windows
req.typenames: ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION, *PACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION
req.redist: 
ms.custom: 19H1
---

# ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION structure


## -description


The <b>ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION</b> structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> function.



## -struct-fields




### -field ElementCount

The number of compatibility elements defined in the application manifest.


### -field Elements

This is an array of <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_compatibility_context_element">COMPATIBILITY_CONTEXT_ELEMENT</a> structures. Each structure describes one compatibility element in the application manifest.


## -remarks



The following example requires Windows Server 2008 R2 or Windows 7 and shows the method to retrieve information about the compatibility context.

<pre class="syntax" xml:space="preserve"><code>HANDLE   ActCtxHandle=INVALID_HANDLE_VALUE;
SIZE_T   BytesWritten=0;
PACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION CtxCompatInfo=NULL;

// Query the compatibility information size
bReturn = QueryActCtxW(0, 
                       ActCtxHandle,
                       NULL,
                       CompatibilityInformationInActivationContext,
                       NULL,
                       0,
                       &amp;BytesWritten);

if (bReturn == FALSE &amp;&amp; GetLastError() !=ERROR_INSUFFICIENT_BUFFER)
       {
	 goto EXIT;
	 }
	 
CtxCompatInfo = 
(PACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION)HeapAlloc(GetProcessHeap(), 
    HEAP_ZERO_MEMORY, BytesWritten);

if (CtxCompatInfo==NULL)
       {
	 // Out of memory
	 goto EXIT;
	 }

// Query the compatibility information
bReturn = QueryActCtxW(0,
                       ActCtxHandle,
                       NULL,
                       CompatibilityInformationInActivationContext,
                       CtxCompatInfo,
                       BytesWritten,
                       &amp;BytesWritten);

if (bReturn==FALSE)
       {
        // Unexpected error: use GetLastError() to check
        goto EXIT;
	 }

for (DWORD ElementIndex=0; ElementIndex &lt; CtxCompatInfo-&gt;ElementCount; ElementIndex ++)
{
PCOMPATIBILITY_CONTEXT_ELEMENT ContextElement = &amp;CtxCompatInfo-&gt;Elements[ElementIndex];
if (ContextElement-&gt;Type == ACTCTX_COMPATIBILITY_ELEMENT_TYPE_OS)
       {
       if (memcmp(&amp;ContextElement-&gt;Id, &amp;WIN7_CONTEXT_GUID, sizeof (GUID))==0)
             {printf_s("Windows 7 is supported");}
	 }
}
	 
EXIT:
if (ActCtxHandle != INVALID_HANDLE_VALUE) 
       {
        ReleaseActCtx (ActCtxHandle)
	 }
if (CtxCompatInfo != NULL)
       {
        RtlFreeHeap (RtlProcessHeap (), 0, CtxCompatInfo);
        CtxCompatInfo = NULL;
	 }
</code></pre>


