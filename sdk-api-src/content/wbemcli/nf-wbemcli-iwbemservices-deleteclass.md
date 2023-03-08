---
UID: NF:wbemcli.IWbemServices.DeleteClass
title: IWbemServices::DeleteClass (wbemcli.h)
description: The IWbemServices::DeleteClass method deletes the specified class from the current namespace.
helpviewer_keywords: ["DeleteClass","DeleteClass method [Windows Management Instrumentation]","DeleteClass method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","DeleteClass method","IWbemServices.DeleteClass","IWbemServices::DeleteClass","WBEM_FLAG_OWNER_UPDATE","WBEM_FLAG_RETURN_IMMEDIATELY","_hmm_iwbemservices_deleteclass","wbemcli/IWbemServices::DeleteClass","wmi.iwbemservices_deleteclass"]
old-location: wmi\iwbemservices_deleteclass.htm
tech.root: wmi
ms.assetid: 1266d93a-776c-481d-b343-826a5c808d24
ms.date: 12/05/2018
ms.keywords: DeleteClass, DeleteClass method [Windows Management Instrumentation], DeleteClass method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],DeleteClass method, IWbemServices.DeleteClass, IWbemServices::DeleteClass, WBEM_FLAG_OWNER_UPDATE, WBEM_FLAG_RETURN_IMMEDIATELY, _hmm_iwbemservices_deleteclass, wbemcli/IWbemServices::DeleteClass, wmi.iwbemservices_deleteclass
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
 - IWbemServices::DeleteClass
 - wbemcli/IWbemServices::DeleteClass
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
 - IWbemServices.DeleteClass
---

# IWbemServices::DeleteClass


## -description

The 
<b>IWbemServices::DeleteClass</b> method deletes the specified class from the current namespace. If a dynamic instance provider is associated with the class, the provider is unregistered, and it is no longer called for by that class. Any classes that derive from the deleted class are also deleted, and their associated providers are unregistered. All outstanding static instances of the specified class and its subclasses are also deleted when the class is deleted.

If a dynamic class provider provides the class, the success of the deletion depends on whether the provider supports class deletion.
<div class="alert"><b>Note</b>  System classes cannot be deleted.</div><div> </div>

## -parameters

### -param strClass [in]

Name of the class targeted for deletion.

### -param lFlags [in]

One of the following values can be set.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes this to be a semisynchronous call. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.



#### WBEM_FLAG_OWNER_UPDATE

Indicates that the caller is a push provider.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider deleting the class. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppCallResult [out]

If <b>NULL</b>, this parameter is not used. If <i>ppCallResult</i> is specified, it must be set to point to <b>NULL</b> on entry. If the <i>lFlags</i> parameter contains <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, this call returns immediately with <b>WBEM_S_NO_ERROR</b>. The <i>ppCallResult</i> parameter receives a pointer to a new 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a> object, which can then be polled to obtain the result using the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus">GetCallStatus</a> method.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclassasync">IWbemServices::DeleteClassAsync</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>