---
UID: NF:wbemcli.IWbemServices.CreateInstanceEnum
title: IWbemServices::CreateInstanceEnum (wbemcli.h)
description: The IWbemServices::CreateInstanceEnum method creates an enumerator that returns the instances of a specified class according to user-specified selection criteria.
helpviewer_keywords: ["CreateInstanceEnum","CreateInstanceEnum method [Windows Management Instrumentation]","CreateInstanceEnum method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","CreateInstanceEnum method","IWbemServices.CreateInstanceEnum","IWbemServices::CreateInstanceEnum","WBEM_FLAG_BIDIRECTIONAL","WBEM_FLAG_DEEP","WBEM_FLAG_DIRECT_READ","WBEM_FLAG_FORWARD_ONLY","WBEM_FLAG_RETURN_IMMEDIATELY","WBEM_FLAG_SHALLOW","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_createinstanceenum","wbemcli/IWbemServices::CreateInstanceEnum","wmi.iwbemservices_createinstanceenum"]
old-location: wmi\iwbemservices_createinstanceenum.htm
tech.root: wmi
ms.assetid: 47671b9b-a2ff-4375-b2a4-7e8599f1fb69
ms.date: 12/05/2018
ms.keywords: CreateInstanceEnum, CreateInstanceEnum method [Windows Management Instrumentation], CreateInstanceEnum method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],CreateInstanceEnum method, IWbemServices.CreateInstanceEnum, IWbemServices::CreateInstanceEnum, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DEEP, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_FORWARD_ONLY, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_SHALLOW, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_createinstanceenum, wbemcli/IWbemServices::CreateInstanceEnum, wmi.iwbemservices_createinstanceenum
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
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemServices::CreateInstanceEnum
 - wbemcli/IWbemServices::CreateInstanceEnum
dev_langs:
 - c++
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
---

# IWbemServices::CreateInstanceEnum


## -description

The 
<b>IWbemServices::CreateInstanceEnum</b> method creates an enumerator that returns the instances of a specified class according to user-specified selection criteria. This method supports simple WQL queries; more complex queries can be processed using the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a> method.

## -parameters

### -param strFilter [in]

Valid <b>BSTR</b> containing the name of the class for which instances are desired. This parameter cannot be <b>NULL</b>.

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
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.



#### WBEM_FLAG_FORWARD_ONLY

This flag causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators but do not allow calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone">Clone</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-reset">Reset</a>.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes Windows Management to retain pointers to objects of the enumeration until the client releases the enumerator. Because object pointers are not released immediately, this method may fail with a <i>hResult</i> of <b>WBEM_E_OUT_OF_MEMORY</b> if the client attempts to enumerate a large number of objects. This flag is implied by default if you set the <i>lFlags</i> parameter to 0 (zero).



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without any regard to its parent class or subclasses.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider that is providing the requested instances. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppEnum [out]

Receives the pointer to the enumerator, which has a positive reference count. The caller must call <b>IUnknown::Release</b> on the pointer after it is no longer required.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

It is not an error for the returned enumerator to have zero elements.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync">IWbemServices::CreateInstanceEnumAsync</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>