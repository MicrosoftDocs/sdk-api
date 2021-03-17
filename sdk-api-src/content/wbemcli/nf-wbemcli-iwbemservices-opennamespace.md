---
UID: NF:wbemcli.IWbemServices.OpenNamespace
title: IWbemServices::OpenNamespace (wbemcli.h)
description: The IWbemServices::OpenNamespace method provides the caller with a new IWbemServices pointer that has the specified child namespace as its operating context.
helpviewer_keywords: ["IWbemServices interface [Windows Management Instrumentation]","OpenNamespace method","IWbemServices.OpenNamespace","IWbemServices::OpenNamespace","OpenNamespace","OpenNamespace method [Windows Management Instrumentation]","OpenNamespace method [Windows Management Instrumentation]","IWbemServices interface","_hmm_iwbemservices_opennamespace","wbemcli/IWbemServices::OpenNamespace","wmi.iwbemservices_opennamespace"]
old-location: wmi\iwbemservices_opennamespace.htm
tech.root: wmi
ms.assetid: 09ff9078-3d97-432b-8626-62f12b5e3ef4
ms.date: 12/05/2018
ms.keywords: IWbemServices interface [Windows Management Instrumentation],OpenNamespace method, IWbemServices.OpenNamespace, IWbemServices::OpenNamespace, OpenNamespace, OpenNamespace method [Windows Management Instrumentation], OpenNamespace method [Windows Management Instrumentation],IWbemServices interface, _hmm_iwbemservices_opennamespace, wbemcli/IWbemServices::OpenNamespace, wmi.iwbemservices_opennamespace
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
 - IWbemServices::OpenNamespace
 - wbemcli/IWbemServices::OpenNamespace
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
 - IWbemServices.OpenNamespace
---

# IWbemServices::OpenNamespace


## -description

The 
<b>IWbemServices::OpenNamespace</b> method provides the caller with a new 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer that has the specified child namespace as its operating context. All operations through the new pointer, such as class or instance creation, only affect that namespace. The namespace must be a child namespace of the current object through which this method is called.

## -parameters

### -param strNamespace [in]

Path to the target namespace. For more information, see 
<a href="/windows/desktop/WmiSdk/creating-hierarchies-within-wmi">Creating Hierarchies within WMI</a>. This namespace can only be relative to the current namespace associated with the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface pointer. This parameter cannot be an absolute path or <b>NULL</b>.

### -param lFlags [in]

This parameter can be set to 0 to make this a synchronous call. To make this a semisynchronous call, set <i>lFlags</i> to <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, provide a valid pointer for the <i>ppResult</i> parameter, and this call will return immediately. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

### -param pCtx [in]

Reserved. This parameter must be <b>NULL</b>.

### -param ppWorkingNamespace [out]

Receives the object that represents the new namespace context. The returned pointer has a positive reference count. The caller must call <b>Release</b> on this pointer when it is no longer needed. This pointer is set to <b>NULL</b> when there are errors. If this parameter is specified, then <i>ppResult</i> must be <b>NULL</b>.

### -param ppResult [out]

Typically <b>NULL</b>. If not <b>NULL</b>, then <i>ppWorkingNamespace</i> must be <b>NULL</b>. In this case, the parameter receives a pointer to a new 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a> object. If the <i>lFlags</i> parameter is set to <b>WBEM_FLAG_RETURN_IMMEDIATELY</b> this call returns immediately. Then the caller can periodically poll the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getresultservices">IWbemCallResult::GetResultServices</a> method until the pointer for the requested namespace becomes available. This parameter is set to point to <b>NULL</b> when there is an error and a new object is not returned.

<div class="alert"><b>Note</b>  It is important to note that when you use this parameter, you must set <i>ppResult</i> to point to <b>NULL</b> before calling the method. This is a COM rule.</div>
<div> </div>

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver">IWbemLocator::ConnectServer</a> method can also be used to open the same namespace. The only difference is that the 
<b>OpenNamespace</b> method allows you to place relative object paths in the <i>Namespace</i> parameter to open child namespaces recursively; 
<b>IWbemLocator::ConnectServer</b> requires a full object path. For more information, see 
<a href="/windows/desktop/WmiSdk/describing-a-wmi-namespace-object-path">Describing a WMI Namespace Object Path</a>.

For example, if the current namespace associated with the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface pointer is root, then using Default in the <i>Namespace</i> parameter yields a new pointer bound to the root\default namespace.

The namespace is closed when <b>Release</b> is called and the reference count reaches 0 (zero).

## -see-also

<a href="/windows/desktop/WmiSdk/creating-hierarchies-within-wmi">Creating Hierarchies within WMI</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver">IWbemLocator::ConnectServer</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>