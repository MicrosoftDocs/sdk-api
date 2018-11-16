---
UID: NF:wbemcli.IWbemUnsecuredApartment.CreateSinkStub
title: IWbemUnsecuredApartment::CreateSinkStub
author: windows-sdk-content
description: The CreateSinkStub method is similar to the IUnsecuredApartment::CreateObjectStub and creates an object forwarder sink and performs access checks for receiving asynchronous calls from Windows Management.
old-location: wmi\iwbemunsecuredapartment_createsinkstub.htm
tech.root: WmiSdk
ms.assetid: 546ae2f8-c208-4846-a3ba-e124aefe619d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateSinkStub, CreateSinkStub method [Windows Management Instrumentation], CreateSinkStub method [Windows Management Instrumentation],IWbemUnsecuredApartment interface, IWbemUnsecuredApartment interface [Windows Management Instrumentation],CreateSinkStub method, IWbemUnsecuredApartment.CreateSinkStub, IWbemUnsecuredApartment::CreateSinkStub, WBEM_FLAG_UNSECAPP_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS, wbemcli/IWbemUnsecuredApartment::CreateSinkStub, wmi.iwbemunsecuredapartment_createsinkstub
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Unsecapp.exe
api_name:
 - IWbemUnsecuredApartment.CreateSinkStub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wbemcli.h
: 
- IWbemUnsecuredApartment.CreateSinkStub
: 
---

# IWbemUnsecuredApartment::CreateSinkStub


## -description


The <a href="https://msdn.microsoft.com/76a376e4-bd0d-4b8b-b49a-162630c47220">CreateSinkStub</a> method is 
    similar to the 
    <b>IUnsecuredApartment::CreateObjectStub</b> 
    and creates an object forwarder sink and performs access checks for receiving asynchronous calls from Windows 
    Management. <b>CreateSinkStub</b> differs from 
    <b>CreateObjectStub</b> because it can 
    specify that callbacks to the sink should be authenticated.

WMI provides the Unsecapp.exe process to function as the separate process. You can host 
    Unsecapp.exe with a call to the 
    <a href="https://msdn.microsoft.com/e77a9ea0-a4cc-4e86-8506-414ecced88f2">IWbemUnsecuredApartment</a> interface or 
    <a href="https://msdn.microsoft.com/6293d8e3-cc5b-4401-8fdc-86f5d03720ea">IUnsecuredApartment</a> interface in other versions of 
    Windows. <b>IUnsecuredApartment</b> does not have any methods 
    that perform  access checking.

An access check means that Unsecapp.exe only allows the  account of the computer that 
    originally obtained the sink to invoke callbacks. When the registry key 
    <b>UnsecAppAccessControlDefault</b> is set to zero then Unsecapp.exe 
    does not perform access control on callbacks unless 
    <a href="https://msdn.microsoft.com/76a376e4-bd0d-4b8b-b49a-162630c47220">CreateSinkStub</a> is called by an 
    application with the <i>dwFlag</i> parameter set to 
    <b>WBEM_FLAG_UNSECAPP_CHECK_ACCESS</b>. If the parameter is not present, which is the default, 
    then Unsecapp.exe reads the registry key value to determine whether to authenticate 
    callbacks.


## -parameters




### -param pSink [in]

Pointer to the client's in-process implementation of 
      <a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>.


### -param dwFlags [in]

You can set one of the following values from 
       <a href="https://msdn.microsoft.com/DE009790-86D0-4030-AC28-F04DD6601261">WBEM_UNSECAPP_FLAG_TYPE</a> enumeration. This 
       parameter determines how Unsecapp.exe uses the registry key checks this registry key:


<b>HKEY_LOCAL_MACHINE</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>WBEM</b>\<b>CIMOM</b>\<b>UnsecAppAccessControlDefault</b>





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
      <a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> calls. The user receives an 
      <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer and must call 
      <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> for 
      <b>IID_WbemObjectSink</b> before using this object in asynchronous 
      <b>IWbemServices</b> calls.


## -returns



This method returns standard COM error codes for 
       <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a>. It returns 
       <b>S_OK</b> if the call succeeds. If the call fails because the requested interface was not 
       supported, the method returns <b>E_NOINTERFACE</b>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to 
       Windows Management.




## -remarks



This method is provided to improve the security of asynchronous calls 
    from client applications. For more information, see 
    <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.




## -see-also




<a href="https://msdn.microsoft.com/76a376e4-bd0d-4b8b-b49a-162630c47220">IUnsecuredApartment::CreateObjectStub</a>



<a href="https://msdn.microsoft.com/e77a9ea0-a4cc-4e86-8506-414ecced88f2">IWbemUnsecuredApartment</a>



<a href="https://msdn.microsoft.com/3d3111ac-7d83-48d6-94e4-36cb46a506fa">Lowering the Security for a Sink in a Separate Process</a>



<a href="https://msdn.microsoft.com/d0259bb1-fd74-4440-ac2a-d6aa84a48d9b">Performing Access Checks</a>



<a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>
 

 

