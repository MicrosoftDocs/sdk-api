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

# _PEB structure


## -description


<p class="CCE_Message">[This structure may be altered in future versions of Windows.]

Contains process information.


## -struct-fields




### -field Reserved1

Reserved for internal use by the operating system.


### -field BeingDebugged

Indicates whether the specified process is currently being debugged. The <b>PEB</b> structure, however, is an internal operating-system structure whose layout may change in the future. It is best to use the <a href="https://msdn.microsoft.com/e7eb2d48-4ef3-4708-8895-2bc33d2c3e91">CheckRemoteDebuggerPresent</a> function instead.


### -field Reserved2

Reserved for internal use by the operating system.


### -field Reserved3

Reserved for internal use by the operating system.


### -field Ldr

A pointer to a <a href="https://msdn.microsoft.com/2e03b513-5c03-4436-99f8-3a6d3a45aff2">PEB_LDR_DATA</a> structure that contains information about the loaded modules for the process.


### -field ProcessParameters

A pointer to an <a href="https://msdn.microsoft.com/e736aefa-9945-4526-84d8-adb6e82b9991">RTL_USER_PROCESS_PARAMETERS</a> structure that contains process parameter information such as the command line.


### -field Reserved4

Reserved for internal use by the operating system.


### -field AtlThunkSListPtr

 


### -field Reserved5

Reserved for internal use by the operating system.


### -field Reserved6

Reserved for internal use by the operating system.


### -field Reserved7

Reserved for internal use by the operating system.


### -field Reserved8

 


### -field AtlThunkSListPtr32

 


### -field Reserved9

 


### -field Reserved10

 


### -field PostProcessInitRoutine

Not supported.


### -field Reserved11

 


### -field Reserved12

 


### -field SessionId

The Terminal Services session identifier associated with the current process.


## -remarks



The syntax for this structure on 64-bit Windows is as follows:

<pre class="syntax" xml:space="preserve"><code>typedef struct _PEB {
    BYTE Reserved1[2];
    BYTE BeingDebugged;
    BYTE Reserved2[21];
    PPEB_LDR_DATA LoaderData;
    PRTL_USER_PROCESS_PARAMETERS ProcessParameters;
    BYTE Reserved3[520];
    PPS_POST_PROCESS_INIT_ROUTINE PostProcessInitRoutine;
    BYTE Reserved4[136];
    ULONG SessionId;
} PEB;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/0eae7899-c40b-4a5f-9e9c-adae021885e7">NtQueryInformationProcess</a>



<a href="https://msdn.microsoft.com/2e03b513-5c03-4436-99f8-3a6d3a45aff2">PEB_LDR_DATA</a>



<a href="https://msdn.microsoft.com/e736aefa-9945-4526-84d8-adb6e82b9991">RTL_USER_PROCESS_PARAMETERS</a>



<a href="https://msdn.microsoft.com/c36c023f-7f9a-4ba5-a41f-f2f755a24eb6">ZwQueryInformationProcess</a>
 

 

