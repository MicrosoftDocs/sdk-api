---
UID: NF:wbemcli.IWbemServices.CreateInstanceEnum
title: IWbemServices::CreateInstanceEnum
author: windows-sdk-content
description: The IWbemServices::CreateInstanceEnum method creates an enumerator that returns the instances of a specified class according to user-specified selection criteria.
old-location: wmi\iwbemservices_createinstanceenum.htm
old-project: WmiSdk
ms.assetid: 47671b9b-a2ff-4375-b2a4-7e8599f1fb69
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: CreateInstanceEnum, CreateInstanceEnum method [Windows Management Instrumentation], CreateInstanceEnum method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],CreateInstanceEnum method, IWbemServices.CreateInstanceEnum, IWbemServices::CreateInstanceEnum, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DEEP, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_FORWARD_ONLY, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_SHALLOW, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_createinstanceenum, wbemcli/IWbemServices::CreateInstanceEnum, wmi.iwbemservices_createinstanceenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Esscli.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Ntevt.dll
 - Stdprov.dll
 - Viewprov.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wbemsvc.dll
 - Wmipicmp.dll
 - Wmidcprv.dll
 - Wmipjobj.dll
 - Wmiprvsd.dll
api_name:
 - IWbemServices.CreateInstanceEnum
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::CreateInstanceEnum


## -description


The 
<b>IWbemServices::CreateInstanceEnum</b> method creates an enumerator that returns the instances of a specified class according to user-specified selection criteria. This method supports simple WQL queries; more complex queries can be processed using the 
<a href="https://msdn.microsoft.com/8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a">IWbemServices::ExecQuery</a> method.


## -parameters




### -param strFilter




### -param lFlags [in]

The following flags affect the behavior of this method. The suggested value for this parameter is <b>WBEM_FLAG_RETURN_IMMEDIATELY</b> and <b>WBEM_FLAG_FORWARD_ONLY</b> for best performance.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_DEEP

This flag forces the enumeration to include this and all subclasses in the hierarchy.



#### WBEM_FLAG_SHALLOW

This flag forces the enumeration to include only pure instances of this class, excluding all instances of subclasses which supply properties not found in this class.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes this to be a semisynchronous call. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.



#### WBEM_FLAG_FORWARD_ONLY

This flag causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators but do not allow calls to 
<a href="https://msdn.microsoft.com/a323c662-e005-44aa-a903-1eb7d6ddff9e">Clone</a> or 
<a href="https://msdn.microsoft.com/571b7067-676f-4e9e-9694-268ec10dc60b">Reset</a>.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes Windows Management to retain pointers to objects of the enumeration until the client releases the enumerator. Because object pointers are not released immediately, this method may fail with a <i>hResult</i> of <b>WBEM_E_OUT_OF_MEMORY</b> if the client attempts to enumerate a large number of objects. This flag is implied by default if you set the <i>lFlags</i> parameter to 0 (zero).



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without any regard to its parent class or subclasses.


### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that may be used by the provider that is providing the requested instances. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param ppEnum [out]

Receives the pointer to the enumerator, which has a positive reference count. The caller must call <b>IUnknown::Release</b> on the pointer after it is no longer required.


#### - strClass [in]

Valid <b>BSTR</b> containing the name of the class for which instances are desired. This parameter cannot be <b>NULL</b>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



It is not an error for the returned enumerator to have zero elements.




## -see-also




<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/5ba2ff28-034f-4949-9bde-8c98345ec7c6">IWbemServices::CreateInstanceEnumAsync</a>



<a href="https://msdn.microsoft.com/f54b8e7c-c531-47d5-bab8-780652b94555">Retrieving an Error Code</a>
 

 

