---
UID: NF:wbemcli.IWbemServices.CancelAsyncCall
title: IWbemServices::CancelAsyncCall
author: windows-sdk-content
description: The IWbemServices::CancelAsyncCall method cancels any currently pending asynchronous calls based on the IWbemObjectSink pointer, which was originally passed to the asynchronous method.
old-location: wmi\iwbemservices_cancelasynccall.htm
old-project: WmiSdk
ms.assetid: 803a7831-1e3d-4940-8d2b-1a74dd16f51a
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CancelAsyncCall, CancelAsyncCall method [Windows Management Instrumentation], CancelAsyncCall method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],CancelAsyncCall method, IWbemServices.CancelAsyncCall, IWbemServices::CancelAsyncCall, _hmm_iwbemservices_cancelasynccall, wbemcli/IWbemServices::CancelAsyncCall, wmi.iwbemservices_cancelasynccall
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
 - IWbemServices.CancelAsyncCall
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::CancelAsyncCall


## -description


The 
<b>IWbemServices::CancelAsyncCall</b> method cancels any currently pending asynchronous calls based on the 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> pointer, which was  originally passed to the asynchronous method. The outstanding 
<b>IWbemObjectSink</b> pointer can be released prior to the call or after the call returns. The 
<b>CancelAsyncCall</b> method is not operational from within a sink and is not supported by method providers. This means only the client end of the call is canceled. The implementing provider is not notified that the call was canceled and runs to completion. You should consider this before canceling methods that take a long time to complete, such as the <a href="https://msdn.microsoft.com/f4782327-0cc6-447e-bc27-7b2042075fb0">Defrag</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn922919">Format</a> methods in the <a href="https://msdn.microsoft.com/71991c97-0e9a-4a0e-a6d6-ee8df263c23d">Win32_Volume</a> class.


## -parameters




### -param pSink [in]

Pointer to the 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> implementation provided by the client to any of the asynchronous methods of 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain available information from the COM function <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

COM-specific error codes can also be returned if network problems cause you to lose the remote connection to Windows Management.

<div class="alert"><b>Note</b>  If 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> has not been called on the application's sink by the time WMI processes 
<b>CancelAsyncCall</b>, WMI calls 
<b>SetStatus</b> on that sink with <b>WBEM_E_CALL_CANCELLED</b> as the value for the <i>hResult</i> parameter.</div>
<div> </div>
Timing, and the nature of an asynchronous operation, can affect whether WMI is able to cancel the operation. Only lengthy queries are likely to be successfully canceled before they have completed. Faster operations, such as asynchronous deletions or modifications, typically complete before WMI can process a 
<b>CancelAsyncCall</b> call. So while 
<b>CancelAsyncCall</b> attempts to cancel the current operation, sometimes all that can be done is to release the 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> pointer.

<div class="alert"><b>Note</b>  It is possible to make numerous asynchronous calls using the same object sink. In this case, the 
<b>CancelAsyncCall</b> method cancels all asynchronous calls sharing this object sink. It is strongly recommended that you create one instance of an object sink for each  outstanding asynchronous call.</div>
<div> </div>



## -remarks



Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>. Calling <b>CancelAsyncCall</b> from within an implementation of <a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">IWbemObjectSink::Indicate</a> or <a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a> can interfere with the WMI state and is not recommended.

In the case of a method call such as <a href="https://msdn.microsoft.com/61966c03-80dc-4556-b2fc-97e879cf458c">ExecMethodAsync</a>, only the client end of the call is canceled. The implementing provider is not  notified that the call was canceled and  runs to completion.

For more information on how to use asynchronous calls, see <a href="https://msdn.microsoft.com/5179969f-bc7d-4408-84ef-7b003950a59f">Making an Asynchronous Call with C++</a> and <a href="https://msdn.microsoft.com/69ec8ead-9073-4689-bc66-5134728ab147">Receiving Asynchronous Event Notifications</a>



#### Examples

For a full example that uses <b>CancelAsyncCall</b>, see <a href="https://msdn.microsoft.com/4d581965-e22a-4205-908c-661eeeec88cf">Example: Receiving Event Notifications Through WMI</a>


<div class="code"></div>
The following C++ sample, taken from the \\Program Files\Microsoft SDKs\Windows\v7.0\Samples\sysmgmt\wmi\vc\decoupled\instance_provider sample, demonstrates an implementation of <b>CancelAsyncCall</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CProvider_IWbemServices :: CancelAsyncCall ( 
  
 IWbemObjectSink *a_Sink
)
{
 HRESULT t_Result = WBEM_E_NOT_AVAILABLE ;
 return t_Result ;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>
 

 

