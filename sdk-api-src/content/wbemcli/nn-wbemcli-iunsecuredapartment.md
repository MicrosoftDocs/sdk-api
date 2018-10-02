---
UID: NN:wbemcli.IUnsecuredApartment
title: IUnsecuredApartment
author: windows-sdk-content
description: The IUnsecuredApartment interface is used to simplify the process of making asynchronous calls from a client process.
old-location: wmi\iunsecuredapartment.htm
tech.root: WmiSdk
ms.assetid: 6293d8e3-cc5b-4401-8fdc-86f5d03720ea
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IUnsecuredApartment, IUnsecuredApartment interface [Windows Management Instrumentation], IUnsecuredApartment interface [Windows Management Instrumentation],described, UnsecuredApartment, _hmm_iunsecuredapartment, wbemcli/IUnsecuredApartment, wmi.iunsecuredapartment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Unsecapp.exe
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Unsecapp.exe
api_name:
 - IUnsecuredApartment
 - UnsecuredApartment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnsecuredApartment interface


## -description


The 
<b>IUnsecuredApartment</b> interface is used to simplify the process of making asynchronous calls from a client process. When a client is making asynchronous calls, the roles of the client and the server are reversed. In this case, the client implements an object (<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> interface) and the server calls the methods of that object. Because of this, COM security rules for servers make it difficult for clients to make asynchronous calls. The primary difficulty is the fact that the client needs to inform COM that it will allow Windows Management to invoke methods on the client's object (<b>IWbemObjectSink</b>).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUnsecuredApartment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUnsecuredApartment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUnsecuredApartment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76a376e4-bd0d-4b8b-b49a-162630c47220">CreateObjectStub</a>
</td>
<td align="left" width="63%">
Creates an object stub to assist in making asynchronous calls from a client process.

</td>
</tr>
</table> 


## -remarks



<b>IUnsecuredApartment</b> allows WMI to create a separate process to handle callbacks. Using this interface creates security risks, as described in <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>. Semisynchronous access or performing access checks are recommended instead of asynchronous calls. For more information and an example of using <b>IUnsecuredApartment</b>, see <a href="https://msdn.microsoft.com/3d3111ac-7d83-48d6-94e4-36cb46a506fa">Lowering the Security for a Sink in a Separate Process</a>. Use <a href="https://msdn.microsoft.com/e77a9ea0-a4cc-4e86-8506-414ecced88f2">IWbemUnsecuredApartment::CreateSinkStub</a> for a more secure approach.




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>



<a href="https://msdn.microsoft.com/e77a9ea0-a4cc-4e86-8506-414ecced88f2">IWbemUnsecuredApartment</a>



<a href="https://msdn.microsoft.com/3d3111ac-7d83-48d6-94e4-36cb46a506fa">Lowering the Security for a Sink in a Separate Process</a>



<a href="https://msdn.microsoft.com/d0259bb1-fd74-4440-ac2a-d6aa84a48d9b">Performing Access Checks</a>



<a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>
 

 

