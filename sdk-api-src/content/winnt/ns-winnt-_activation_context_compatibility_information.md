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

# _ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION structure


## -description


The <b>ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION</b> structure is used by the <a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> function.



## -struct-fields




### -field ElementCount

The number of compatibility elements defined in the application manifest.


### -field Elements

This is an array of <a href="https://msdn.microsoft.com/3e654f44-43f6-4282-b277-14ed6e25abf2">COMPATIBILITY_CONTEXT_ELEMENT</a> structures. Each structure describes one compatibility element in the application manifest.


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


