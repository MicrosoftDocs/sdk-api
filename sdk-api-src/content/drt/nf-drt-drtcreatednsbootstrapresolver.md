---
UID: NF:drt.DrtCreateDnsBootstrapResolver
title: DrtCreateDnsBootstrapResolver function
author: windows-sdk-content
description: The DrtCreateDnsBootstrapResolver function creates a bootstrap resolver that will use the GetAddrInfo system function to resolve the hostname of a will known node already present in the DRT mesh.
old-location: p2p\drtcreatednsbootstrapresolver.htm
tech.root: p2psdk
ms.assetid: d4a92dd3-d66a-4c27-9180-f9c148735a4a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrtCreateDnsBootstrapResolver, DrtCreateDnsBootstrapResolver function [Distributed Routing Tables], drt/DrtCreateDnsBootstrapResolver, p2p.drtcreatednsbootstrapresolver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtCreateDnsBootstrapResolver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrtCreateDnsBootstrapResolver function


## -description


The <b>DrtCreateDnsBootstrapResolver</b> function creates a bootstrap resolver that will use the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfo</a> system function to resolve the hostname of a will known node already present in the DRT mesh.


## -parameters




### -param port [in]

Specifies the port to which the DRT protocol is bound on the well known node.


### -param pwszAddress [in]

Specifies the hostname of the well known node.


### -param ppModule [out]

Pointer to the <a href="https://msdn.microsoft.com/f64edf7f-379f-41e2-9a86-ba9aeee0f2d7">DRT_BOOTSTRAP_PROVIDER</a> module to be included in the <a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a> structure.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwszAddress</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system could not allocate memory for the provider.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This function may also return errors from underlying calls to <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> and StringCbPrintfW.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f64edf7f-379f-41e2-9a86-ba9aeee0f2d7">DRT_BOOTSTRAP_PROVIDER</a>



<a href="https://msdn.microsoft.com/fc3d0b6a-1bf3-41f9-82b6-965c285bc6c7">DrtDeleteDnsBootstrapResolver</a>
 

 

