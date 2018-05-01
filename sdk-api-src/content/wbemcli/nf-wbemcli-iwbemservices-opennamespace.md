---
UID: NF:wbemcli.IWbemServices.OpenNamespace
title: IWbemServices::OpenNamespace method
author: windows-driver-content
description: The IWbemServices::OpenNamespace method provides the caller with a new IWbemServices pointer that has the specified child namespace as its operating context.
old-location: wmi\iwbemservices_opennamespace.htm
old-project: WmiSdk
ms.assetid: 09ff9078-3d97-432b-8626-62f12b5e3ef4
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWbemServices, IWbemServices interface [Windows Management Instrumentation], OpenNamespace method, IWbemServices::OpenNamespace, OpenNamespace method [Windows Management Instrumentation], OpenNamespace method [Windows Management Instrumentation], IWbemServices interface, OpenNamespace,IWbemServices.OpenNamespace, _hmm_iwbemservices_opennamespace, wbemcli/IWbemServices::OpenNamespace, wmi.iwbemservices_opennamespace
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fastprox.dll
-	Esscli.dll
-	FrameDyn.dll
-	FrameDynOS.dll
-	Ntevt.dll
-	Stdprov.dll
-	Viewprov.dll
-	Wbemcomn.dll
-	Wbemcore.dll
-	Wbemess.dll
-	Wbemsvc.dll
-	Wmipicmp.dll
-	Wmidcprv.dll
-	Wmipjobj.dll
-	Wmiprvsd.dll
api_name:
-	IWbemServices.OpenNamespace
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::OpenNamespace method


## -description


The 
<b>IWbemServices::OpenNamespace</b> method provides the caller with a new 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer that has the specified child namespace as its operating context. All operations through the new pointer, such as class or instance creation, only affect that namespace. The namespace must be a child namespace of the current object through which this method is called.


## -parameters




### -param strNamespace [in]

Path to the target namespace. For more information, see 
<a href="https://msdn.microsoft.com/a00f26e6-bb81-45bc-a530-9346a074bb3c">Creating Hierarchies within WMI</a>. This namespace can only be relative to the current namespace associated with the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface pointer. This parameter cannot be an absolute path or <b>NULL</b>.


### -param lFlags [in]

This parameter can be set to 0 to make this a synchronous call. To make this a semisynchronous call, set <i>lFlags</i> to <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, provide a valid pointer for the <i>ppResult</i> parameter, and this call will return immediately. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


### -param pCtx [in]

Reserved. This parameter must be <b>NULL</b>.


### -param ppWorkingNamespace [out]

Receives the object that represents the new namespace context. The returned pointer has a positive reference count. The caller must call <b>Release</b> on this pointer when it is no longer needed. This pointer is set to <b>NULL</b> when there are errors. If this parameter is specified, then <i>ppResult</i> must be <b>NULL</b>.


### -param ppResult [out]

Typically <b>NULL</b>. If not <b>NULL</b>, then <i>ppWorkingNamespace</i> must be <b>NULL</b>. In this case, the parameter receives a pointer to a new 
<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a> object. If the <i>lFlags</i> parameter is set to <b>WBEM_FLAG_RETURN_IMMEDIATELY</b> this call returns immediately. Then the caller can periodically poll the 
<a href="https://msdn.microsoft.com/64a4fc4c-f479-4b03-847c-041508e55532">IWbemCallResult::GetResultServices</a> method until the pointer for the requested namespace becomes available. This parameter is set to point to <b>NULL</b> when there is an error and a new object is not returned.

<div class="alert"><b>Note</b>  It is important to note that when you use this parameter, you must set <i>ppResult</i> to point to <b>NULL</b> before calling the method. This is a COM rule.</div>
<div> </div>

## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



The 
<a href="https://msdn.microsoft.com/92222e08-8622-46c3-9465-cd12260a2ca0">IWbemLocator::ConnectServer</a> method can also be used to open the same namespace. The only difference is that the 
<b>OpenNamespace</b> method allows you to place relative object paths in the <i>Namespace</i> parameter to open child namespaces recursively; 
<b>IWbemLocator::ConnectServer</b> requires a full object path. For more information, see 
<a href="https://msdn.microsoft.com/6d8da19e-0914-4267-870e-c203176b895e">Describing a WMI Namespace Object Path</a>.

For example, if the current namespace associated with the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface pointer is root, then using Default in the <i>Namespace</i> parameter yields a new pointer bound to the root\default namespace.

The namespace is closed when <b>Release</b> is called and the reference count reaches 0 (zero).




## -see-also




<a href="https://msdn.microsoft.com/a00f26e6-bb81-45bc-a530-9346a074bb3c">Creating Hierarchies within WMI</a>



<a href="https://msdn.microsoft.com/92222e08-8622-46c3-9465-cd12260a2ca0">IWbemLocator::ConnectServer</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/f54b8e7c-c531-47d5-bab8-780652b94555">Retrieving an Error Code</a>
 

 

