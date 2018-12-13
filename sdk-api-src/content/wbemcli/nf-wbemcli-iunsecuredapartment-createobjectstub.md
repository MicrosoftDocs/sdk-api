---
UID: NF:wbemcli.IUnsecuredApartment.CreateObjectStub
title: IUnsecuredApartment::CreateObjectStub
author: windows-sdk-content
description: The CreateObjectStub method creates an object forwarder sink to assist in receiving asynchronous calls from Windows Management.
old-location: wmi\iunsecuredapartment_createobjectstub.htm
tech.root: WmiSdk
ms.assetid: 76a376e4-bd0d-4b8b-b49a-162630c47220
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateObjectStub, CreateObjectStub method [Windows Management Instrumentation], CreateObjectStub method [Windows Management Instrumentation],IUnsecuredApartment interface, IUnsecuredApartment interface [Windows Management Instrumentation],CreateObjectStub method, IUnsecuredApartment.CreateObjectStub, IUnsecuredApartment::CreateObjectStub, _hmm_iunsecuredapartment_createobjectstub, wbemcli/IUnsecuredApartment::CreateObjectStub, wmi.iunsecuredapartment_createobjectstub
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008 R2
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
 - IUnsecuredApartment.CreateObjectStub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnsecuredApartment::CreateObjectStub


## -description


The 
<b>CreateObjectStub</b> method creates an object forwarder sink to assist in receiving asynchronous calls from Windows Management. This function binds an unsecured object sink to a local object sink so that COM security does not interfere with asynchronous retrieval of CIM objects. Because COM security is being bypassed, the remote Windows Management server is assumed to be a trusted component.

The general paradigm is that the original implementation of 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> in the client process is not directly used in asynchronous calls to 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>. Rather, both the original implementation and a substitute object are created, bound together, and then the substitute object is used in the asynchronous methods of 
<b>IWbemServices</b>.


## -parameters




### -param pObject [in]

Pointer to the client's in-process implementation of 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>.


### -param ppStub [out]

Receives a pointer to a substitute object to be used in asynchronous 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> calls. The user receives an <a href="_com_iunknown">IUnknown</a> pointer and must call <a href="_com_iunknown_queryinterface">QueryInterface</a> for <b>IID_WbemObjectSink</b> before using this object in asynchronous 
<b>IWbemServices</b> calls.


## -returns



This method returns standard COM error codes for <a href="_com_iunknown_queryinterface">QueryInterface</a>. It returns <b>S_OK</b> if the call succeeds. If the call fails because the requested interface was not supported, the method returns <b>E_NOINTERFACE</b>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



<div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.</div>
<div> </div>

#### Examples

For a complete example that shows how to use the <a href="https://msdn.microsoft.com/6293d8e3-cc5b-4401-8fdc-86f5d03720ea">IUnsecuredApartment</a> interface, see <a href="https://msdn.microsoft.com/4d581965-e22a-4205-908c-661eeeec88cf">Example: Receiving Event Notifications Through WMI</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/6293d8e3-cc5b-4401-8fdc-86f5d03720ea">IUnsecuredApartment</a>



<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>



<a href="https://msdn.microsoft.com/546ae2f8-c208-4846-a3ba-e124aefe619d">IWbemUnsecuredApartment::CreateSinkStub</a>



<a href="https://msdn.microsoft.com/3d3111ac-7d83-48d6-94e4-36cb46a506fa">Lowering the Security for a Sink in a Separate Process</a>



<a href="https://msdn.microsoft.com/d0259bb1-fd74-4440-ac2a-d6aa84a48d9b">Performing Access Checks</a>



<a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>
 

 

