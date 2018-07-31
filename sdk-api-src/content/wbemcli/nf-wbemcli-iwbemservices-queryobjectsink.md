---
UID: NF:wbemcli.IWbemServices.QueryObjectSink
title: IWbemServices::QueryObjectSink
author: windows-sdk-content
description: The IWbemServices::QueryObjectSink method allows the caller to obtain a notification handler that is exported by Windows Management.
old-location: wmi\iwbemservices_queryobjectsink.htm
old-project: WmiSdk
ms.assetid: 218b42f2-838d-4d8f-98d2-9334ec29d279
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWbemServices interface [Windows Management Instrumentation],QueryObjectSink method, IWbemServices.QueryObjectSink, IWbemServices::QueryObjectSink, QueryObjectSink, QueryObjectSink method [Windows Management Instrumentation], QueryObjectSink method [Windows Management Instrumentation],IWbemServices interface, _hmm_iwbemservices_queryobjectsink, wbemcli/IWbemServices::QueryObjectSink, wmi.iwbemservices_queryobjectsink
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
 - IWbemServices.QueryObjectSink
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::QueryObjectSink


## -description


The <b>IWbemServices::QueryObjectSink</b> method 
  allows the caller to obtain a notification handler that is exported by Windows Management. This allows the caller 
  to write notifications and events directly to Windows Management. The caller should only write extrinsic events to 
  Windows Management. For more information, see 
  <a href="https://msdn.microsoft.com/46cdfcfa-42c6-4169-bc4d-725867224889">Determining the Type of Event to Receive</a>.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param ppResponseHandler [out]

Receives the interface pointer to the notification handler. This is set to point to <b>NULL</b> when there is an error. The returned pointer has a positive reference count, and the caller must call <b>IWbemServices::Release</b> on the pointer when it is no longer needed. A <b>NULL</b> value can be returned if no notification handler is available. This is not an error.

<div class="alert"><b>Note</b>  The value of the <i>ppResponseHandler</i> parameter cannot be <b>NULL</b> when it is passed to this method.</div>
<div> </div>

## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

<div class="alert"><b>Note</b>  Firing events using <b>QueryObjectSink</b> 
    is permitted by default for Administrators only. Extending the permission to other users requires giving them 
  <b>WBEM_FULL_WRITE</b> permission.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/0cceda42-fba0-4a08-90dd-43f022d0be41">Querying WMI</a>
 

 

