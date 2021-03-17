---
UID: NF:wbemcli.IWbemServices.ExecNotificationQuery
title: IWbemServices::ExecNotificationQuery (wbemcli.h)
description: The IWbemServices::ExecNotificationQuery method executes a query to receive events. The call returns immediately, and the user can poll the returned enumerator for events as they arrive. Releasing the returned enumerator cancels the query.
helpviewer_keywords: ["ExecNotificationQuery","ExecNotificationQuery method [Windows Management Instrumentation]","ExecNotificationQuery method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","ExecNotificationQuery method","IWbemServices.ExecNotificationQuery","IWbemServices::ExecNotificationQuery","WBEM_FLAG_FORWARD_ONLY","WBEM_FLAG_RETURN_IMMEDIATELY","_hmm_iwbemservices_execnotificationquery","wbemcli/IWbemServices::ExecNotificationQuery","wmi.iwbemservices_execnotificationquery"]
old-location: wmi\iwbemservices_execnotificationquery.htm
tech.root: wmi
ms.assetid: fe547660-4095-4a75-829d-f06599c0d9d7
ms.date: 12/05/2018
ms.keywords: ExecNotificationQuery, ExecNotificationQuery method [Windows Management Instrumentation], ExecNotificationQuery method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecNotificationQuery method, IWbemServices.ExecNotificationQuery, IWbemServices::ExecNotificationQuery, WBEM_FLAG_FORWARD_ONLY, WBEM_FLAG_RETURN_IMMEDIATELY, _hmm_iwbemservices_execnotificationquery, wbemcli/IWbemServices::ExecNotificationQuery, wmi.iwbemservices_execnotificationquery
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
 - IWbemServices::ExecNotificationQuery
 - wbemcli/IWbemServices::ExecNotificationQuery
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
 - IWbemServices.ExecNotificationQuery
---

# IWbemServices::ExecNotificationQuery


## -description

The 
<b>IWbemServices::ExecNotificationQuery</b> method executes a query to receive events. The call returns immediately, and the user can poll the returned enumerator for events as they arrive. Releasing the returned enumerator cancels the query.

## -parameters

### -param strQueryLanguage [in]

Valid <b>BSTR</b> that contains one of the query languages supported by Windows Management. This cannot be <b>NULL</b>. Currently, only the 
<a href="/windows/desktop/WmiSdk/querying-with-wql">WMI Query Language</a> (WQL) is supported.

### -param strQuery [in]

Valid <b>BSTR</b> that contains the text of the event-related query. This cannot be <b>NULL</b>. For more information on building WMI query strings, see <a href="/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a> and the <a href="/windows/desktop/WmiSdk/wql-sql-for-wmi">WQL</a> reference.

### -param lFlags [in]

This parameter must be set to both <b>WBEM_FLAG_RETURN_IMMEDIATELY</b> and <b>WBEM_FLAG_FORWARD_ONLY</b> or the call fails.



#### WBEM_FLAG_FORWARD_ONLY

This flag causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators but do not allow calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone">Clone</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-reset">Reset</a>.



#### WBEM_FLAG_RETURN_IMMEDIATELY

The user must specify this flag or the call fails. This is because events are received continuously, which means the user must poll the returned enumerator. Blocking this call indefinitely while waiting for a possible event  blocks the thread for an indefinite amount of time. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that can be used by the provider that provides the requested events. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppEnum [out]

If no error occurs, this parameter receives the enumerator that allows the caller to retrieve the instances in the result set of the query. The caller periodically calls 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-next">IEnumWbemClassObject::Next</a> to see if any events are available. Notice that, in this usage, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-reset">Reset</a> does not move the enumerator back to the beginning of the event sequence; it has no effect. The parameter can continue to receive events until <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> is called on the returned enumerator.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes also can be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

There are limits to the number of <b>AND</b> and <b>OR</b> keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM_E_QUOTA_VIOLATION error code as an <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync">IWbemServices::ExecNotificationQueryAsync</a>



<a href="/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a>



<a href="/windows/desktop/WmiSdk/receiving-events-for-the-duration-of-your-application">Receiving Events for the Duration of your Application</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>