---
UID: NF:wbemcli.IWbemServices.ExecNotificationQuery
title: IWbemServices::ExecNotificationQuery
author: windows-sdk-content
description: The IWbemServices::ExecNotificationQuery method executes a query to receive events. The call returns immediately, and the user can poll the returned enumerator for events as they arrive. Releasing the returned enumerator cancels the query.
old-location: wmi\iwbemservices_execnotificationquery.htm
old-project: WmiSdk
ms.assetid: fe547660-4095-4a75-829d-f06599c0d9d7
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ExecNotificationQuery, ExecNotificationQuery method [Windows Management Instrumentation], ExecNotificationQuery method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecNotificationQuery method, IWbemServices.ExecNotificationQuery, IWbemServices::ExecNotificationQuery, WBEM_FLAG_FORWARD_ONLY, WBEM_FLAG_RETURN_IMMEDIATELY, _hmm_iwbemservices_execnotificationquery, wbemcli/IWbemServices::ExecNotificationQuery, wmi.iwbemservices_execnotificationquery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IWbemServices.ExecNotificationQuery
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::ExecNotificationQuery


## -description


The 
<b>IWbemServices::ExecNotificationQuery</b> method executes a query to receive events. The call returns immediately, and the user can poll the returned enumerator for events as they arrive. Releasing the returned enumerator cancels the query.


## -parameters




### -param strQueryLanguage [in]

Valid <b>BSTR</b> that contains one of the query languages supported by Windows Management. This cannot be <b>NULL</b>. Currently, only the 
<a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">WMI Query Language</a> (WQL) is supported.


### -param strQuery [in]

Valid <b>BSTR</b> that contains the text of the event-related query. This cannot be <b>NULL</b>. For more information on building WMI query strings, see <a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a> and the <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL</a> reference.


### -param lFlags [in]

This parameter must be set to both <b>WBEM_FLAG_RETURN_IMMEDIATELY</b> and <b>WBEM_FLAG_FORWARD_ONLY</b> or the call fails.



#### WBEM_FLAG_FORWARD_ONLY

This flag causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators but do not allow calls to 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a> or 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>.



#### WBEM_FLAG_RETURN_IMMEDIATELY

The user must specify this flag or the call fails. This is because events are received continuously, which means the user must poll the returned enumerator. Blocking this call indefinitely while waiting for a possible event  blocks the thread for an indefinite amount of time. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that can be used by the provider that provides the requested events. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param ppEnum [out]

If no error occurs, this parameter receives the enumerator that allows the caller to retrieve the instances in the result set of the query. The caller periodically calls 
<a href="https://msdn.microsoft.com/8bde633b-b04a-4a21-82ce-f5aab1d32d95">IEnumWbemClassObject::Next</a> to see if any events are available. Notice that, in this usage, 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> does not move the enumerator back to the beginning of the event sequence; it has no effect. The parameter can continue to receive events until <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> is called on the returned enumerator.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

COM-specific error codes also can be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



There are limits to the number of <b>AND</b> and <b>OR</b> keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM_E_QUOTA_VIOLATION error code as an <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.




## -see-also




<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/f26eb44a-e0c4-418b-b849-d38d85ef236a">IWbemServices::ExecNotificationQueryAsync</a>



<a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a>



<a href="https://msdn.microsoft.com/380ac556-ba0a-4fae-8b76-0645d99e8583">Receiving Events for the Duration of your Application</a>



<a href="https://msdn.microsoft.com/f54b8e7c-c531-47d5-bab8-780652b94555">Retrieving an Error Code</a>
 

 

