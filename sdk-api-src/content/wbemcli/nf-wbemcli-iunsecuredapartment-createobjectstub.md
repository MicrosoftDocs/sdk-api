---
UID: NF:wbemcli.IUnsecuredApartment.CreateObjectStub
title: IUnsecuredApartment::CreateObjectStub (wbemcli.h)
description: The CreateObjectStub method creates an object forwarder sink to assist in receiving asynchronous calls from Windows Management.
helpviewer_keywords: ["CreateObjectStub","CreateObjectStub method [Windows Management Instrumentation]","CreateObjectStub method [Windows Management Instrumentation]","IUnsecuredApartment interface","IUnsecuredApartment interface [Windows Management Instrumentation]","CreateObjectStub method","IUnsecuredApartment.CreateObjectStub","IUnsecuredApartment::CreateObjectStub","_hmm_iunsecuredapartment_createobjectstub","wbemcli/IUnsecuredApartment::CreateObjectStub","wmi.iunsecuredapartment_createobjectstub"]
old-location: wmi\iunsecuredapartment_createobjectstub.htm
tech.root: wmi
ms.assetid: 76a376e4-bd0d-4b8b-b49a-162630c47220
ms.date: 12/05/2018
ms.keywords: CreateObjectStub, CreateObjectStub method [Windows Management Instrumentation], CreateObjectStub method [Windows Management Instrumentation],IUnsecuredApartment interface, IUnsecuredApartment interface [Windows Management Instrumentation],CreateObjectStub method, IUnsecuredApartment.CreateObjectStub, IUnsecuredApartment::CreateObjectStub, _hmm_iunsecuredapartment_createobjectstub, wbemcli/IUnsecuredApartment::CreateObjectStub, wmi.iunsecuredapartment_createobjectstub
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUnsecuredApartment::CreateObjectStub
 - wbemcli/IUnsecuredApartment::CreateObjectStub
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
 - IUnsecuredApartment.CreateObjectStub
---

# IUnsecuredApartment::CreateObjectStub


## -description

The 
<b>CreateObjectStub</b> method creates an object forwarder sink to assist in receiving asynchronous calls from Windows Management. This function binds an unsecured object sink to a local object sink so that COM security does not interfere with asynchronous retrieval of CIM objects. Because COM security is being bypassed, the remote Windows Management server is assumed to be a trusted component.

The general paradigm is that the original implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> in the client process is not directly used in asynchronous calls to 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>. Rather, both the original implementation and a substitute object are created, bound together, and then the substitute object is used in the asynchronous methods of 
<b>IWbemServices</b>.

## -parameters

### -param pObject [in]

Pointer to the client's in-process implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>.

### -param ppStub [out]

Receives a pointer to a substitute object to be used in asynchronous 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> calls. The user receives an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer and must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for <b>IID_WbemObjectSink</b> before using this object in asynchronous 
<b>IWbemServices</b> calls.

## -returns

This method returns standard COM error codes for <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>. It returns <b>S_OK</b> if the call succeeds. If the call fails because the requested interface was not supported, the method returns <b>E_NOINTERFACE</b>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

<div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.</div>
<div> </div>

#### Examples

For a complete example that shows how to use the <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a> interface, see <a href="/windows/desktop/WmiSdk/example--receiving-event-notifications-through-wmi-">Example: Receiving Event Notifications Through WMI</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a>



<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub">IWbemUnsecuredApartment::CreateSinkStub</a>



<a href="/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>



<a href="/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>



<a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>