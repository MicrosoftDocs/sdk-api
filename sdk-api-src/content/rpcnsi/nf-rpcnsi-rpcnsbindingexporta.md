---
UID: NF:rpcnsi.RpcNsBindingExportA
title: RpcNsBindingExportA function
author: windows-sdk-content
description: The RpcNsBindingExport function establishes a name service&#8211;database entry with multiple binding handles and multiple objects for a server.
old-location: rpc\rpcnsbindingexport.htm
tech.root: Rpc
ms.assetid: c89d04d7-f607-48cc-8cb6-b6aebab41671
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RpcNsBindingExport, RpcNsBindingExport function [RPC], RpcNsBindingExportA, RpcNsBindingExportW, _rpc_rpcnsbindingexport, rpc.rpcnsbindingexport, rpcnsi/RpcNsBindingExport, rpcnsi/RpcNsBindingExportA, rpcnsi/RpcNsBindingExportW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsBindingExportW (Unicode) and RpcNsBindingExportA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsBindingExport
 - RpcNsBindingExportA
 - RpcNsBindingExportW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcNsBindingExportA function


## -description


The 
<b>RpcNsBindingExport</b> function establishes a name service–database entry with multiple binding handles and multiple objects for a server.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param EntryName

Pointer to the entry name to which binding handles and object UUIDs are exported. You cannot provide a null or empty string. The client and the server must both use the same entry name.


### -param IfSpec

Stub-generated data structure specifying the interface to export. A null value indicates there are no binding handles to export (only object UUIDs are to be exported) and <i>BindingVec</i> is ignored.


### -param BindingVec

Pointer to server bindings to export. A null value indicates there are no binding handles to export (only object UUIDs are to be exported).


### -param ObjectUuidVec

Pointer to a vector of object UUIDs offered by the server. The server application constructs this vector. A null value indicates there are no object UUIDs to export (only binding handles are to be exported).


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NOTHING_TO_EXPORT</b></dt>
</dl>
</td>
<td width="60%">
There was nothing to export.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNSUPPORTED_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INCOMPLETE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is incomplete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_NS_PRIVILEGE</b></dt>
</dl>
</td>
<td width="60%">
No privilege for name-service operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name service is unavailable.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsBindingExport</b> function allows a server application to publicly offer an interface in the name-service database for use by any client application.

Effective with Windows 2000, the RPC run-time environment uses the Active Directory as its name-service database. This means that authorized exported entries persist in the name service, and are visible even after rebooting. Unauthorized exports do not persist. See 
<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a> in the Security section of the Platform Software Development Kit (SDK) for more information on authorization and Access Control Lists.

To export an interface, the server application calls the 
<b>RpcNsBindingExport</b> routine with an interface and the server binding handles a client can use to access the server. A server application also calls the 
<b>RpcNsBindingExport</b> function to publicly offer the object UUID(s) of resource(s) it offers, if any, in the name-service database.

A server can export interfaces and objects in a single call to 
<b>RpcNsBindingExport</b>, or it can export them separately.If the name-service database entry specified by <i>EntryName</i> does not exist, 
<b>RpcNsBindingExport</b> tries to create it. In this case, the server application must have the privilege to create the entry.In addition to calling 
<b>RpcNsBindingExport</b>, a server that called the 
<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a> or 
<b>RpcServerUseProtseq</b> function must also register with the local endpoint-map database by calling either 
<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a> or 
<a href="https://msdn.microsoft.com/eaf132a8-0bc2-4201-945a-76b6c2eab559">RpcEpRegisterNoReplace</a>.

A server is not required to export any of its interfaces to the name-service database. When a server does not export, only clients that privately know that server's binding information can access its interfaces. For example, a client that has the information needed to construct a string binding can call the 
<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a> to create a binding handle for making remote procedure calls to a server.

Before calling 
<b>RpcNsBindingExport</b>, a server must do the following:

<ul>
<li>Register one or more protocol sequences with the local RPC run-time library by calling one of the following functions: 


<ul>
<li>
<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a>, 
<a href="https://msdn.microsoft.com/4fc2ccbe-1b01-4157-b3e7-2c61397d78f7">RpcServerUseAllProtseqsEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9b2c9cf0-fe96-4063-a893-f2793595af57">RpcServerUseProtseq</a>, 
<a href="https://msdn.microsoft.com/a8cedfe9-9c16-4c35-9cc4-5ccaa9e130a8">RpcServerUseProtseqEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6f3f7726-3e12-4b0b-8454-25f06a29b245">RpcServerUseAllProtseqsIf</a>, 
<a href="https://msdn.microsoft.com/118c931e-29ca-4ffb-aa32-24c6f4289cc8">RpcServerUseAllProtseqsIfEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/41c1fa20-266a-4071-91b3-d0fd8196871b">RpcServerUseProtseqIf</a>, 
<a href="https://msdn.microsoft.com/41c1fa20-266a-4071-91b3-d0fd8196871b">RpcServerUseProtseqIf</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1914a90a-6dee-4517-9de1-d332124eb0a4">RpcServerUseProtseqEp</a>, 
<a href="https://msdn.microsoft.com/1914a90a-6dee-4517-9de1-d332124eb0a4">RpcServerUseProtseqEp</a>
</li>
</ul>
</li>
<li>Obtain a list of server bindings by calling the 
<a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a> function.</li>
</ul>
The vector returned from the 
<a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a> function becomes the <i>Binding</i> parameter for 
<b>RpcNsBindingExport</b>. To prevent a binding from being exported, set the selected vector element to a null value.

If a server exports to the same name-service database entry multiple times, the second and subsequent calls to 
<b>RpcNsBindingExport</b> add the binding information and object UUIDs when that data is different from the binding information already in the server entry. Existing data is not removed from the entry.

To remove binding handles and object UUIDs from the name-service database, a server application calls the 
<a href="https://msdn.microsoft.com/70662e7e-7a81-4953-9814-e29b46422c5b">RpcNsBindingUnexport</a> function.

A server entry must have at least one binding handle to exist. As a result, exporting only UUIDs to a non-existing entry has no effect, and unexporting all binding handles deletes the entry.




## -see-also




<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/eaf132a8-0bc2-4201-945a-76b6c2eab559">RpcEpRegisterNoReplace</a>



<a href="https://msdn.microsoft.com/70662e7e-7a81-4953-9814-e29b46422c5b">RpcNsBindingUnexport</a>



<a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a>



<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a>



<a href="https://msdn.microsoft.com/6f3f7726-3e12-4b0b-8454-25f06a29b245">RpcServerUseAllProtseqsIf</a>



<a href="https://msdn.microsoft.com/9b2c9cf0-fe96-4063-a893-f2793595af57">RpcServerUseProtseq</a>



<a href="https://msdn.microsoft.com/1914a90a-6dee-4517-9de1-d332124eb0a4">RpcServerUseProtseqEp</a>



<a href="https://msdn.microsoft.com/41c1fa20-266a-4071-91b3-d0fd8196871b">RpcServerUseProtseqIf</a>
 

 

