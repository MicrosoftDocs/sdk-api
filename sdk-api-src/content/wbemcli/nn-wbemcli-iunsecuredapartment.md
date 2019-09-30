---
UID: NN:wbemcli.IUnsecuredApartment
title: IUnsecuredApartment (wbemcli.h)
author: windows-sdk-content
description: The IUnsecuredApartment interface is used to simplify the process of making asynchronous calls from a client process.
old-location: wmi\iunsecuredapartment.htm
tech.root: WmiSdk
ms.assetid: 6293d8e3-cc5b-4401-8fdc-86f5d03720ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUnsecuredApartment, IUnsecuredApartment interface [Windows Management Instrumentation], IUnsecuredApartment interface [Windows Management Instrumentation],described, UnsecuredApartment, _hmm_iunsecuredapartment, wbemcli/IUnsecuredApartment, wmi.iunsecuredapartment
ms.topic: interface
f1_keywords: 
 - "wbemcli/IUnsecuredApartment"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUnsecuredApartment interface


## -description


The 
<b>IUnsecuredApartment</b> interface is used to simplify the process of making asynchronous calls from a client process. When a client is making asynchronous calls, the roles of the client and the server are reversed. In this case, the client implements an object (<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> interface) and the server calls the methods of that object. Because of this, COM security rules for servers make it difficult for clients to make asynchronous calls. The primary difficulty is the fact that the client needs to inform COM that it will allow Windows Management to invoke methods on the client's object (<b>IWbemObjectSink</b>).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUnsecuredApartment</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUnsecuredApartment</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub">CreateObjectStub</a>
</td>
<td align="left" width="63%">
Creates an object stub to assist in making asynchronous calls from a client process.

</td>
</tr>
</table> 


## -remarks



<b>IUnsecuredApartment</b> allows WMI to create a separate process to handle callbacks. Using this interface creates security risks, as described in <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>. Semisynchronous access or performing access checks are recommended instead of asynchronous calls. For more information and an example of using <b>IUnsecuredApartment</b>, see <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>. Use <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemunsecuredapartment">IWbemUnsecuredApartment::CreateSinkStub</a> for a more secure approach.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemunsecuredapartment">IWbemUnsecuredApartment</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>
 

 

