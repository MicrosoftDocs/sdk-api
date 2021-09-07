---
UID: NN:wbemcli.IWbemClassObject
title: IWbemClassObject (wbemcli.h)
description: Contains and manipulates both class definitions and class object instances.
helpviewer_keywords: ["IWbemClassObject","IWbemClassObject interface [Windows Management Instrumentation]","IWbemClassObject interface [Windows Management Instrumentation]","described","WbemClassObject","_hmm_iwbemclassobject","wbemcli/IWbemClassObject","wmi.iwbemclassobject"]
old-location: wmi\iwbemclassobject.htm
tech.root: wmi
ms.assetid: a3ce37d7-5580-4b84-9119-78412c8e0d27
ms.date: 12/05/2018
ms.keywords: IWbemClassObject, IWbemClassObject interface [Windows Management Instrumentation], IWbemClassObject interface [Windows Management Instrumentation],described, WbemClassObject, _hmm_iwbemclassobject, wbemcli/IWbemClassObject, wmi.iwbemclassobject
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemClassObject
 - wbemcli/IWbemClassObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CIMWin32.dll
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipiprt.dll
api_name:
 - IWbemClassObject
 - WbemClassObject
---

# IWbemClassObject interface


## -description

The <b>IWbemClassObject</b> interface 
    contains and manipulates both class definitions and class object instances.

## -inheritance

The <b>IWbemClassObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemClassObject</b> also has these types of members:

## -remarks

Users and providers should never implement this interface. The implementation provided by WMI is the only one 
     that is supported.

From the WMI client perspective, this interface is always in-process. Write 
     (<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put">Put</a>) operations only affect the local copy of the 
     object, and read (<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">Get</a>) operations always retrieve 
     values from the local copy. You can perform updates to WMI only when entire objects are read or written using 
     methods on the <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface. Examples of such 
     updates are: <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a> or 
     <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">IWbemServices::PutClass</a>.

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/WmiSdk/creating-and-declaring-an-instance-using-c-">Creating and Declaring an Instance Using C++</a>



<a href="/windows/desktop/WmiSdk/describing-a-class-object-path">Describing a Class Object Path</a>



<a href="/windows/desktop/WmiSdk/describing-an-instance-object-path">Describing an Instance Object Path</a>



<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>
