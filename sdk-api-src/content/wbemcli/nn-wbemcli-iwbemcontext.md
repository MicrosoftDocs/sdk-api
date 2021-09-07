---
UID: NN:wbemcli.IWbemContext
title: IWbemContext (wbemcli.h)
description: The IWbemContext interface is optionally used to communicate additional context information to providers when submitting IWbemServices calls to WMI. All primary calls in IWbemServices take an optional parameter pointing to an object of this type.
helpviewer_keywords: ["IWbemContext","IWbemContext interface [Windows Management Instrumentation]","IWbemContext interface [Windows Management Instrumentation]","described","WbemContext","_hmm_iwbemcontext","wbemcli/IWbemContext","wmi.iwbemcontext"]
old-location: wmi\iwbemcontext.htm
tech.root: wmi
ms.assetid: 458bd455-6984-414b-a0b7-62887d9dad7c
ms.date: 12/05/2018
ms.keywords: IWbemContext, IWbemContext interface [Windows Management Instrumentation], IWbemContext interface [Windows Management Instrumentation],described, WbemContext, _hmm_iwbemcontext, wbemcli/IWbemContext, wmi.iwbemcontext
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
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemContext
 - wbemcli/IWbemContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipjobj.dll
api_name:
 - IWbemContext
 - WbemContext
---

# IWbemContext interface


## -description

The 
<b>IWbemContext</b> interface is optionally used to communicate  additional context information to providers when submitting 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> calls to WMI. All primary calls in 
<b>IWbemServices</b> take an optional parameter pointing to an object of this type.

## -inheritance

The <b>IWbemContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemContext</b> also has these types of members:

## -remarks

Often, dynamic providers require more information than is specified in the normal parameters of an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> method. For example, to manipulate any WMI schema objects that it provides, a provider may need to know a Simple Network Management Protocol (SNMP) community name, or a Structured Query Language (SQL) database and table name. A client can add this information to an 
<b>IWbemContext</b> object and send the 
<b>IWbemContext</b> object along with the call as one of the parameters.

Providers should use content objects sparingly. It is recommended that it is never required. If a provider requires a large amount of highly specific context information to respond to a request, then all clients must be coded to provide this information, thus breaking the uniform access model that is the basis of WMI. Nevertheless, in some cases it cannot be avoided. Therefore, this mechanism is provided to make it possible to access such providers. Developers of such providers should provide adequate documentation so that developers of client software can successfully manipulate such CIM objects.

Providers that support the use of 
<b>IWbemContext</b> to allow clients to specify more information in a request should restrict the types of values they support to the types in the following list:

<ul>
<li><b>VT_I4</b></li>
<li><b>VT_R8</b></li>
<li><b>VT_BOOL</b></li>
<li><b>VT_BSTR</b></li>
<li><b>VT_UNKNOWN</b></li>
<li>Any of the above combined with <b>VT_ARRAY</b></li>
</ul>
<div class="alert"><b>Note</b>  Only objects that support 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> can marshal their <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> methods in an 
<b>IWbemContext</b> instance using a variant of type <b>VT_UNKNOWN</b>.</div>
<div> </div>
An 
<b>IWbemContext</b> object, which is created using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>, is a simple container of named values. Access these methods to fill in  context information required by a dynamic provider. After the call to one of the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> methods, the 
<b>IWbemContext</b> object can be reused for another call, or it can be deallocated using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> and another object created for other calls to 
<b>IWbemServices</b> methods.

The information contained in an 
<b>IWbemContext</b> object is entirely determined by the underlying provider. WMI does not use the information, but forwards it to the provider. Providers must publish the context information they require for these service requests.

The client application calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> to create a single context object. Then, it calls 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-setvalue">SetValue</a> one or more times to set up context values for the provider. Finally, it submits the object to one of the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> methods, which immediately calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the context object after the call has returned. The other methods are for use primarily by providers that receive the context object and have to extract information.

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/WmiSdk/creating-and-declaring-an-instance-using-c-">Creating and Declaring an Instance Using C++</a>



<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>



<a href="/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform">Requesting WMI Data on a 64-bit Platform</a>



<a href="/windows/desktop/WmiSdk/retrieving-part-of-an-instance">Retrieving Part of a WMI Instance</a>
