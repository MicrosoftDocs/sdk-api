---
UID: NF:wbemcli.IWbemServices.ExecNotificationQueryAsync
title: IWbemServices::ExecNotificationQueryAsync
author: windows-sdk-content
description: The IWbemServices::ExecNotificationQueryAsync method performs the same task as IWbemServices::ExecNotificationQuery except that events are supplied to the specified response handler until CancelAsyncCall is called to stop the event notification.
old-location: wmi\iwbemservices_execnotificationqueryasync.htm
tech.root: WmiSdk
ms.assetid: f26eb44a-e0c4-418b-b849-d38d85ef236a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ExecNotificationQueryAsync, ExecNotificationQueryAsync method [Windows Management Instrumentation], ExecNotificationQueryAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecNotificationQueryAsync method, IWbemServices.ExecNotificationQueryAsync, IWbemServices::ExecNotificationQueryAsync, WBEM_FLAG_SEND_STATUS, _hmm_iwbemservices_execnotificationqueryasync, wbemcli/IWbemServices::ExecNotificationQueryAsync, wmi.iwbemservices_execnotificationqueryasync
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
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
 - IWbemServices.ExecNotificationQueryAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemServices::ExecNotificationQueryAsync


## -description


The 
<b>IWbemServices::ExecNotificationQueryAsync</b> method performs the same task as 
<a href="https://msdn.microsoft.com/fe547660-4095-4a75-829d-f06599c0d9d7">IWbemServices::ExecNotificationQuery</a> except that events are supplied to the specified response handler until 
<a href="https://msdn.microsoft.com/803a7831-1e3d-4940-8d2b-1a74dd16f51a">CancelAsyncCall</a> is called to stop the event notification.


## -parameters




### -param strQueryLanguage [in]

Valid <b>BSTR</b> that contains one of the query languages supported by Windows Management. This must be "WQL".


### -param strQuery [in]

Valid <b>BSTR</b> that contains the text of the event-related query. This cannot be <b>NULL</b>. For more information on building WMI query strings, see <a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a> and the <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL</a> reference.


### -param lFlags [in]

This parameter can be the following value.



#### WBEM_FLAG_SEND_STATUS

This flag registers with Windows Management a request to receive intermediate status reports through the client's implementation of 
<a href="https://msdn.microsoft.com/en-us/library/Aa391789(v=VS.85).aspx">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting for this flag to change behavior.


### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that may be used by the provider that is returning the requested events. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>. This handler receives the objects in the query result set as they become available. To cease receiving events, the caller must call 
<a href="https://msdn.microsoft.com/803a7831-1e3d-4940-8d2b-1a74dd16f51a">IWbemServices::CancelAsyncCall</a> using the same pointer value for <i>pResponseHandler</i>. As events become available, the supplied 
<a href="https://msdn.microsoft.com/en-us/library/Aa391788(v=VS.85).aspx">IWbemObjectSink::Indicate</a> implementation is called to deliver the event objects. The 
<a href="https://msdn.microsoft.com/en-us/library/Aa391789(v=VS.85).aspx">IWbemObjectSink::SetStatus</a> method is not called at any time, because there is no final or terminating condition. The call executes indefinitely until canceled. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management only calls <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> on the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For a detailed explanation of this parameter, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a>.

Other error codes are returned to the object sink specified by the <i>pResponseHandler</i> parameter.

COM-specific error codes also can be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



The 
<a href="https://msdn.microsoft.com/en-us/library/Aa391789(v=VS.85).aspx">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. It may also be called with no intervening calls to 
<a href="https://msdn.microsoft.com/en-us/library/Aa391788(v=VS.85).aspx">IWbemObjectSink::Indicate</a> if error conditions occur.

Because the call-back might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="https://msdn.microsoft.com/fe547660-4095-4a75-829d-f06599c0d9d7">IWbemServices::ExecNotificationQuery</a> and <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

There are limits to the number of <b>AND</b> and <b>OR</b> keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the <b>WBEM_E_QUOTA_VIOLATION</b> error code as an <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a">IWbemServices::ExecQuery</a>



<a href="https://msdn.microsoft.com/851ad9bd-2604-4988-8de0-8d29b5300b21">Receiving Event Notifications</a>



<a href="https://msdn.microsoft.com/380ac556-ba0a-4fae-8b76-0645d99e8583">Receiving Events for the Duration of your Application</a>
 

 

