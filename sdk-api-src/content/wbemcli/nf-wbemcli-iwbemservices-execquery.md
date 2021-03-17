---
UID: NF:wbemcli.IWbemServices.ExecQuery
title: IWbemServices::ExecQuery (wbemcli.h)
description: The IWbemServices::ExecQuery method executes a query to retrieve objects.
helpviewer_keywords: ["ExecQuery","ExecQuery method [Windows Management Instrumentation]","ExecQuery method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","ExecQuery method","IWbemServices.ExecQuery","IWbemServices::ExecQuery","WBEM_FLAG_BIDIRECTIONAL","WBEM_FLAG_DIRECT_READ","WBEM_FLAG_ENSURE_LOCATABLE","WBEM_FLAG_FORWARD_ONLY","WBEM_FLAG_PROTOTYPE","WBEM_FLAG_RETURN_IMMEDIATELY","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_execquery","wbemcli/IWbemServices::ExecQuery","wmi.iwbemservices_execquery"]
old-location: wmi\iwbemservices_execquery.htm
tech.root: wmi
ms.assetid: 8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a
ms.date: 12/05/2018
ms.keywords: ExecQuery, ExecQuery method [Windows Management Instrumentation], ExecQuery method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecQuery method, IWbemServices.ExecQuery, IWbemServices::ExecQuery, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_ENSURE_LOCATABLE, WBEM_FLAG_FORWARD_ONLY, WBEM_FLAG_PROTOTYPE, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_execquery, wbemcli/IWbemServices::ExecQuery, wmi.iwbemservices_execquery
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
 - IWbemServices::ExecQuery
 - wbemcli/IWbemServices::ExecQuery
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
 - IWbemServices.ExecQuery
---

# IWbemServices::ExecQuery


## -description

The 
<b>IWbemServices::ExecQuery</b> method executes a query to retrieve objects.

For the valid types of queries that can be performed, see 
<a href="/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a>.

## -parameters

### -param strQueryLanguage [in]

Valid <b>BSTR</b> that contains one of the query languages supported by Windows Management. This must be "WQL", the acronym for WMI Query Language.

### -param strQuery [in]

Valid <b>BSTR</b> that contains the text of the query. This parameter cannot be <b>NULL</b>. For more information on building WMI query strings, see <a href="/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a> and the <a href="/windows/desktop/WmiSdk/wql-sql-for-wmi">WQL</a> reference.

### -param lFlags [in]

The following flags affect the behavior of this method. The suggested value for this parameter is <b>WBEM_FLAG_RETURN_IMMEDIATELY</b> and <b>WBEM_FLAG_FORWARD_ONLY</b> for best performance.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_FORWARD_ONLY

This flag causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators but do not allow calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone">Clone</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-reset">Reset</a>.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes Windows Management to retain pointers to objects of the enumeration until the client releases the enumerator.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes this to be a semisynchronous call. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.



#### WBEM_FLAG_ENSURE_LOCATABLE

This flag ensures that any returned objects have enough information in them so that the system properties, such as <b>__PATH</b>, <b>__RELPATH</b>, and <b>__SERVER</b>, are non-NULL.



#### WBEM_FLAG_PROTOTYPE

This flag is used for prototyping. It does not execute the query and instead returns an object that looks like a typical result object.



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without any regard to its parent class or subclasses.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that can be used by the provider that is providing the requested classes or instances. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppEnum [out]

If no error occurs, this receives the enumerator that allows the caller to retrieve the instances in the result set of the query. It is not an error for the query to have a result set with 0 instances. This is determined only by attempting to iterate through the instances. This object returns with a positive reference count. The caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the object is no longer required.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes also can be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

The 
<b>IWbemServices::ExecQuery</b> method processes the query specified in the <i>strQuery</i> parameter and creates an enumerator through which the caller can access the query results. The enumerator is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject">IEnumWbemClassObject</a> interface; the query results are instances of class objects made available through the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interface.

There are limits to the number of "AND" and "OR" keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the <b>WBEM_E_QUOTA_VIOLATION</b> error code as an <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a>



<a href="/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a>