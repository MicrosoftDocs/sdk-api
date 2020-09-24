---
UID: NF:wbemcli.IWbemUnsecuredApartment.CreateSinkStub
title: IWbemUnsecuredApartment::CreateSinkStub (wbemcli.h)
description: The CreateSinkStub method is similar to the IUnsecuredApartment::CreateObjectStub and creates an object forwarder sink and performs access checks for receiving asynchronous calls from Windows Management.
helpviewer_keywords: ["CreateSinkStub","CreateSinkStub method [Windows Management Instrumentation]","CreateSinkStub method [Windows Management Instrumentation]","IWbemUnsecuredApartment interface","IWbemUnsecuredApartment interface [Windows Management Instrumentation]","CreateSinkStub method","IWbemUnsecuredApartment.CreateSinkStub","IWbemUnsecuredApartment::CreateSinkStub","WBEM_FLAG_UNSECAPP_CHECK_ACCESS","WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS","WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS","wbemcli/IWbemUnsecuredApartment::CreateSinkStub","wmi.iwbemunsecuredapartment_createsinkstub"]
old-location: wmi\iwbemunsecuredapartment_createsinkstub.htm
tech.root: wmi
ms.assetid: 546ae2f8-c208-4846-a3ba-e124aefe619d
ms.date: 12/05/2018
ms.keywords: CreateSinkStub, CreateSinkStub method [Windows Management Instrumentation], CreateSinkStub method [Windows Management Instrumentation],IWbemUnsecuredApartment interface, IWbemUnsecuredApartment interface [Windows Management Instrumentation],CreateSinkStub method, IWbemUnsecuredApartment.CreateSinkStub, IWbemUnsecuredApartment::CreateSinkStub, WBEM_FLAG_UNSECAPP_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS, wbemcli/IWbemUnsecuredApartment::CreateSinkStub, wmi.iwbemunsecuredapartment_createsinkstub
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - IWbemUnsecuredApartment::CreateSinkStub
 - wbemcli/IWbemUnsecuredApartment::CreateSinkStub
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
 - IWbemUnsecuredApartment.CreateSinkStub
---

# IWbemUnsecuredApartment::CreateSinkStub


## -description

The <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub">CreateSinkStub</a> method is 
    similar to the 
    <b>IUnsecuredApartment::CreateObjectStub</b> 
    and creates an object forwarder sink and performs access checks for receiving asynchronous calls from Windows 
    Management. <b>CreateSinkStub</b> differs from 
    <b>CreateObjectStub</b> because it can 
    specify that callbacks to the sink should be authenticated.

WMI provides the Unsecapp.exe process to function as the separate process. You can host 
    Unsecapp.exe with a call to the 
    <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemunsecuredapartment">IWbemUnsecuredApartment</a> interface or 
    <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a> interface in other versions of 
    Windows. <b>IUnsecuredApartment</b> does not have any methods 
    that perform  access checking.

An access check means that Unsecapp.exe only allows the  account of the computer that 
    originally obtained the sink to invoke callbacks. When the registry key 
    <b>UnsecAppAccessControlDefault</b> is set to zero then Unsecapp.exe 
    does not perform access control on callbacks unless 
    <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub">CreateSinkStub</a> is called by an 
    application with the <i>dwFlag</i> parameter set to 
    <b>WBEM_FLAG_UNSECAPP_CHECK_ACCESS</b>. If the parameter is not present, which is the default, 
    then Unsecapp.exe reads the registry key value to determine whether to authenticate 
    callbacks.

## -parameters

### -param pSink [in]

Pointer to the client's in-process implementation of 
      <a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>.

### -param dwFlags [in]

You can set one of the following values from 
       <a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_unsecapp_flag_type">WBEM_UNSECAPP_FLAG_TYPE</a> enumeration. This 
       parameter determines how Unsecapp.exe uses the registry key checks this registry key:


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>WBEM</b>&#92;<b>CIMOM</b>&#92;<b>UnsecAppAccessControlDefault</b>





#### WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS

Unsecapp.exe reads the registry key 
        <b>UnsecAppAccessControlDefault</b> to determine if it should authenticate 
        callbacks.



#### WBEM_FLAG_UNSECAPP_CHECK_ACCESS

Unsecapp.exe authenticates callbacks regardless of the setting of the registry key 
        <b>UnsecAppAccessControlDefault</b>.



#### WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS

Unsecapp.exe does not authenticate callbacks regardless of the setting of the 
        registry key <b>UnsecAppAccessControlDefault</b>.

### -param wszReserved

Reserved.

### -param ppStub [out]

Receives a pointer to a substitute object to be used in asynchronous 
      <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> calls. The user receives an 
      <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer and must call 
      <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for 
      <b>IID_WbemObjectSink</b> before using this object in asynchronous 
      <b>IWbemServices</b> calls.

## -returns

This method returns standard COM error codes for 
       <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>. It returns 
       <b>S_OK</b> if the call succeeds. If the call fails because the requested interface was not 
       supported, the method returns <b>E_NOINTERFACE</b>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to 
       Windows Management.

## -remarks

This method is provided to improve the security of asynchronous calls 
    from client applications. For more information, see 
    <a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub">IUnsecuredApartment::CreateObjectStub</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemunsecuredapartment">IWbemUnsecuredApartment</a>



<a href="/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>



<a href="/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>



<a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>