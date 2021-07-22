---
UID: NN:wbemcli.IWbemObjectAccess
title: IWbemObjectAccess (wbemcli.h)
description: Provides access to the methods and properties of an object.
helpviewer_keywords: ["IWbemObjectAccess","IWbemObjectAccess interface [Windows Management Instrumentation]","IWbemObjectAccess interface [Windows Management Instrumentation]","described","_hmm_iwbemobjectaccess","wbemcli/IWbemObjectAccess","wmi.iwbemobjectaccess"]
old-location: wmi\iwbemobjectaccess.htm
tech.root: wmi
ms.assetid: 1025ae50-870f-4d38-8e83-3c6b628315c6
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess, IWbemObjectAccess interface [Windows Management Instrumentation], IWbemObjectAccess interface [Windows Management Instrumentation],described, _hmm_iwbemobjectaccess, wbemcli/IWbemObjectAccess, wmi.iwbemobjectaccess
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
req.dll: Esscli.dll; Fastprox.dll; Wbemess.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemObjectAccess
 - wbemcli/IWbemObjectAccess
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
 - Wbemess.dll
api_name:
 - IWbemObjectAccess
---

# IWbemObjectAccess interface


## -description

The 
<b>IWbemObjectAccess</b> interface provides access to the methods and properties of an object.  An 
<b>IWbemObjectAccess</b> object is a container for an instance updated by a <a href="/windows/desktop/WmiSdk/gloss-r">refresher</a>. With the 
<b>IWbemObjectAccess</b> interface, you can get and set properties by using property handles instead of object property names.
<div class="alert"><b>Note</b>  This interface is not implemented by client applications or providers under any circumstances. The implementation provided by WMI is the only one that is supported. A pointer to the interface can be retrieved by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IWbemClassObject::QueryInterface</a>.</div><div> </div>

## -inheritance

The <b>IWbemObjectAccess</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemObjectAccess</b> also has these types of members:

## -remarks

The 
<b>IWbemObjectAccess</b> methods that read and write data perform very little data validation. Because 
<b>IWbemObjectAccess</b> methods directly access properties, you can get and set properties much more rapidly than you can using standard object access techniques such as 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">IWbemClassObject::Get</a> and 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put">IWbemClassObject::Put</a>.

<div class="alert"><b>Note</b>  To maximize its speed, 
<b>IWbemObjectAccess</b> is completely unchecked. It is the responsibility of the user to ensure that all handles are proper, and that write buffers are correctly sized. Read and write operations are not intrinsically thread-safe. You should call the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-lock">IWbemObjectAccess::Lock</a> and 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-unlock">IWbemObjectAccess::Unlock</a> methods to prevent 
<b>IWbemObjectAccess</b> objects from concurrent access on multiple threads.</div>
<div> </div>
Property handles are the same for all instances of a class. Therefore, it is only necessary to retrieve a handle one time.

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/WmiSdk/accessing-wmi-preinstalled-performance-classes">Accessing WMI Preinstalled Performance Classes</a>



<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a>
