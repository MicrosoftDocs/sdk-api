---
UID: NE:combaseapi.tagREGCLS
title: tagREGCLS
author: windows-sdk-content
description: Controls the type of connections to a class object.
old-location: com\regcls.htm
tech.root: com
ms.assetid: 16bca8e0-9999-4d51-b7f0-87deb7619d89
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: REGCLS, REGCLS enumeration [COM], REGCLS_AGILE, REGCLS_MULTIPLEUSE, REGCLS_MULTI_SEPARATE, REGCLS_SINGLEUSE, REGCLS_SURROGATE, REGCLS_SUSPENDED, _com_REGCLS, com.regcls, combaseapi/REGCLS, combaseapi/REGCLS_AGILE, combaseapi/REGCLS_MULTIPLEUSE, combaseapi/REGCLS_MULTI_SEPARATE, combaseapi/REGCLS_SINGLEUSE, combaseapi/REGCLS_SURROGATE, combaseapi/REGCLS_SUSPENDED, tagREGCLS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - combaseapi.h
api_name:
 - REGCLS
product: Windows
targetos: Windows
req.typenames: REGCLS
req.redist: 
---

# tagREGCLS enumeration


## -description


Controls the type of connections to a class object.


## -enum-fields




### -field REGCLS_SINGLEUSE

After an application is connected to a class object with <a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a>, the class object is removed from public view so that no other applications can connect to it. This value is commonly used for single document interface (SDI) applications. Specifying this value does not affect the responsibility of the object application to call <a href="https://msdn.microsoft.com/en-us/library/ms688650(v=VS.85).aspx">CoRevokeClassObject</a>; it must always call <b>CoRevokeClassObject</b> when it is finished with an object class.


### -field REGCLS_MULTIPLEUSE

Multiple applications can connect to the class object through calls to <a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a>. If both the REGCLS_MULTIPLEUSE and CLSCTX_LOCAL_SERVER are set in a call to <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a>, the class object is also automatically registered as an in-process server, whether CLSCTX_INPROC_SERVER is explicitly set.


### -field REGCLS_MULTI_SEPARATE

Useful for registering separate CLSCTX_LOCAL_SERVER and CLSCTX_INPROC_SERVER class factories through calls to <a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a>. If REGCLS_MULTI_SEPARATE is set, each execution context must be set separately; <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a> does not automatically register an out-of-process server (for which CLSCTX_LOCAL_SERVER is set) as an in-process server. This allows the EXE to create multiple instances of the object for in-process needs, such as self embeddings, without disturbing its CLSCTX_LOCAL_SERVER registration. If an EXE registers a REGCLS_MULTI_SEPARATE class factory and a CLSCTX_INPROC_SERVER class factory, instance creation calls that specify CLSCTX_INPROC_SERVER in the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> parameter executed by the EXE would be satisfied locally without approaching the SCM. This mechanism is useful when the EXE uses functions such as <a href="https://msdn.microsoft.com/en-us/library/ms678409(v=VS.85).aspx">OleCreate</a> and <a href="https://msdn.microsoft.com/en-us/library/ms694338(v=VS.85).aspx">OleLoad</a> to create embeddings, but at the same does not wish to launch a new instance of itself for the self-embedding case. The distinction is important for embeddings because the default handler aggregates the proxy manager by default and the application should override this default behavior by calling <a href="https://msdn.microsoft.com/en-us/library/ms683795(v=VS.85).aspx">OleCreateEmbeddingHelper</a> for the self-embedding case. 

If your application need not distinguish between the local and inproc case, you need not register your class factory using REGCLS_MULTI_SEPARATE. In fact, the application incurs an extra network round trip to the SCM when it registers its MULTIPLEUSE class factory as MULTI_SEPARATE and does not register another class factory as INPROC_SERVER.


### -field REGCLS_SUSPENDED

Suspends registration and activation requests for the specified CLSID until there is a call to <a href="https://msdn.microsoft.com/en-us/library/ms692686(v=VS.85).aspx">CoResumeClassObjects</a>. This is used typically to register the CLSIDs for servers that can register multiple class objects to reduce the overall registration time, and thus the server application startup time, by making a single call to the SCM, no matter how many CLSIDs are registered for the server.

<div class="alert"><b>Note</b>  This flag prevents COM activation errors from a possible race condition between an application shutting down and that application attempting to register a COM class.</div>
<div> </div>

### -field REGCLS_SURROGATE

The class object is a surrogate process used to run DLL servers. The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server, but a generic class factory implemented by the surrogate. This generic class factory delegates instance creation and marshaling to the class factory of the DLL server running in the surrogate. For further information on DLL surrogates, see the <a href="https://msdn.microsoft.com/en-us/library/ms691260(v=VS.85).aspx">DllSurrogate</a> registry value.


### -field REGCLS_AGILE

The class object aggregates the free-threaded marshaler
                                 and will be made visible to all inproc apartments. Can be used together with other flags. For example, REGCLS_AGILE | REGCLS_MULTIPLEUSE to register a
                                class object that can be used multiple times from
                                different apartments. Without other flags, behavior
                                will retain REGCLS_SINGLEUSE semantics in that only
                                one instance can be generated.


## -remarks



In <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a>, members of both the <b>REGCLS</b> and the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumerations, taken together, determine how the class object is registered.



An EXE surrogate (in which DLL servers are run) calls <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a> to register a class factory using a new <b>REGCLS</b> value, REGCLS_SURROGATE.

All class factories for DLL surrogates should be registered with REGCLS_SURROGATE set. Do not set REGCLS_SINGLUSE or REGCLS_MULTIPLEUSE when you register a surrogate for DLL servers.

The following table summarizes the allowable <b>REGCLS</b> value combinations and the object registrations affected by the combinations.

<table>
<tr>
<th></th>
<th>REGCLS_SINGLEUSE</th>
<th>REGCLS_MULTIPLEUSE</th>
<th>REGCLS_MULTI_SEPARATE</th>
<th>Other</th>
</tr>
<tr>
<td>CLSCTX_INPROC_SERVER</td>
<td>Error</td>
<td>In-process</td>
<td>In-process</td>
<td>Error</td>
</tr>
<tr>
<td>CLSCTX_LOCAL_SERVER</td>
<td>Local</td>
<td>In-process/local</td>
<td>Local</td>
<td>Error</td>
</tr>
<tr>
<td>Both of the above</td>
<td>Error</td>
<td>In-process/local</td>
<td>In-process/local</td>
<td>Error</td>
</tr>
<tr>
<td>Other</td>
<td>Error</td>
<td>Error</td>
<td>Error</td>
<td>Error</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680760(v=VS.85).aspx">DllGetClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691260(v=VS.85).aspx">DllSurrogate</a>
 

 

