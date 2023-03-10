---
UID: NN:wbemcli.IUnsecuredApartment
title: IUnsecuredApartment (wbemcli.h)
description: The IUnsecuredApartment interface is used to simplify the process of making asynchronous calls from a client process.
helpviewer_keywords: ["IUnsecuredApartment","IUnsecuredApartment interface [Windows Management Instrumentation]","IUnsecuredApartment interface [Windows Management Instrumentation]","described","UnsecuredApartment","_hmm_iunsecuredapartment","wbemcli/IUnsecuredApartment","wmi.iunsecuredapartment"]
old-location: wmi\iunsecuredapartment.htm
tech.root: wmi
ms.assetid: 6293d8e3-cc5b-4401-8fdc-86f5d03720ea
ms.date: 12/05/2018
ms.keywords: IUnsecuredApartment, IUnsecuredApartment interface [Windows Management Instrumentation], IUnsecuredApartment interface [Windows Management Instrumentation],described, UnsecuredApartment, _hmm_iunsecuredapartment, wbemcli/IUnsecuredApartment, wmi.iunsecuredapartment
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUnsecuredApartment
 - wbemcli/IUnsecuredApartment
dev_langs:
 - c++
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
---

# IUnsecuredApartment interface


## -description

The 
<b>IUnsecuredApartment</b> interface is used to simplify the process of making asynchronous calls from a client process. When a client is making asynchronous calls, the roles of the client and the server are reversed. In this case, the client implements an object (<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> interface) and the server calls the methods of that object. Because of this, COM security rules for servers make it difficult for clients to make asynchronous calls. The primary difficulty is the fact that the client needs to inform COM that it will allow Windows Management to invoke methods on the client's object (<b>IWbemObjectSink</b>).

## -inheritance

The <b>IUnsecuredApartment</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUnsecuredApartment</b> also has these types of members:

## -remarks

<b>IUnsecuredApartment</b> allows WMI to create a separate process to handle callbacks. Using this interface creates security risks, as described in <a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>. Semisynchronous access or performing access checks are recommended instead of asynchronous calls. For more information and an example of using <b>IUnsecuredApartment</b>, see <a href="/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>. Use <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemunsecuredapartment">IWbemUnsecuredApartment::CreateSinkStub</a> for a more secure approach.

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemunsecuredapartment">IWbemUnsecuredApartment</a>



<a href="/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>



<a href="/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>



<a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>
