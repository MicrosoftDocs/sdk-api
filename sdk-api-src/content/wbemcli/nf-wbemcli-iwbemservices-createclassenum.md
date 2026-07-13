---
UID: NF:wbemcli.IWbemServices.CreateClassEnum
title: IWbemServices::CreateClassEnum (wbemcli.h)
description: The IWbemServices::CreateClassEnum method returns an enumerator for all classes that satisfy selection criteria.
helpviewer_keywords: ["CreateClassEnum","CreateClassEnum method [Windows Management Instrumentation]","CreateClassEnum method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","CreateClassEnum method","IWbemServices.CreateClassEnum","IWbemServices::CreateClassEnum","WBEM_FLAG_BIDIRECTIONAL","WBEM_FLAG_DEEP","WBEM_FLAG_FORWARD_ONLY","WBEM_FLAG_RETURN_IMMEDIATELY","WBEM_FLAG_SHALLOW","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_createclassenum","wbemcli/IWbemServices::CreateClassEnum","wmi.iwbemservices_createclassenum"]
old-location: wmi\iwbemservices_createclassenum.htm
tech.root: wmi
ms.assetid: 23122b38-5671-4454-be79-85c6bc34daa0
ms.date: 12/05/2018
ms.keywords: CreateClassEnum, CreateClassEnum method [Windows Management Instrumentation], CreateClassEnum method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],CreateClassEnum method, IWbemServices.CreateClassEnum, IWbemServices::CreateClassEnum, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DEEP, WBEM_FLAG_FORWARD_ONLY, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_SHALLOW, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_createclassenum, wbemcli/IWbemServices::CreateClassEnum, wmi.iwbemservices_createclassenum
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
 - IWbemServices::CreateClassEnum
 - wbemcli/IWbemServices::CreateClassEnum
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
 - IWbemServices.CreateClassEnum
---

# IWbemServices::CreateClassEnum


## -description

The 
<b>IWbemServices::CreateClassEnum</b> method returns an enumerator for all classes that satisfy selection criteria. The caller must use the returned enumerator to retrieve the class definitions, calling 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-next">IEnumWbemClassObject::Next</a> to obtain each class or blocks of classes. It finishes by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IEnumWbemClassObject::Release</a>.
<div class="alert"><b>Note</b>  It is not an error for the returned enumerator to have 0 (zero) elements.</div><div> </div>

## -parameters

### -param strSuperclass [in]

If not <b>NULL</b> or blank, specifies a parent class name. Only classes that are subclasses of this class are returned in the enumerator. If it is <b>NULL</b> or blank, and <i>lFlags</i> is WBEM_FLAG_SHALLOW, only the top-level classes are returned (that is, classes that have no parent class). If it is <b>NULL</b> or blank and <i>lFlags</i> is <b>WBEM_FLAG_DEEP</b>, all classes within the namespace are returned.

### -param lFlags [in]

The following flags affect the behavior of this method. The suggested value for this parameter is WBEM_FLAG_RETURN_IMMEDIATELY and WBEM_FLAG_FORWARD_ONLY for best performance.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_DEEP

This flag forces the enumeration to include all subclasses in the hierarchy, but not this class.



#### WBEM_FLAG_SHALLOW

This flag forces the enumeration to include only pure instances of this class, excluding all instances of subclasses that supply properties not found in this class.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes  a semisynchronous call. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.



#### WBEM_FLAG_FORWARD_ONLY

This flag causes a forward-only enumerator to be returned. Typically, forward-only enumerators are  faster and use less memory than conventional enumerators, but they do not allow calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone">Clone</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-reset">Reset</a>.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator. Because object pointers are not released immediately, this method may fail with an <b>HRESULT</b> of <b>WBEM_E_OUT_OF_MEMORY</b> if the client attempts to enumerate a large number of objects. This flag is implied by default if you set the <i>lFlags</i> parameter to 0 (zero).

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that can be used by the provider that is providing the requested classes. The values in the context object must be specified in the documentation for the provider. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppEnum [out]

Receives the pointer to the enumerator. The returned object has a positive reference count. The caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the pointer when it is no longer required.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of a method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain available information from the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes also can be returned if network problems cause you to lose the remote connection to Windows Management.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject">IEnumWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync">IWbemServices::CreateClassEnumAsync</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>