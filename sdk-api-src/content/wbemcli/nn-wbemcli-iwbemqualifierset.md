---
UID: NN:wbemcli.IWbemQualifierSet
title: IWbemQualifierSet (wbemcli.h)
description: Acts as a container for the entire set of named qualifiers for a single property or entire object (a class or instance).
helpviewer_keywords: ["IWbemQualifierSet","IWbemQualifierSet interface [Windows Management Instrumentation]","IWbemQualifierSet interface [Windows Management Instrumentation]","described","_hmm_iwbemqualifierset","wbemcli/IWbemQualifierSet","wmi.iwbemqualifierset"]
old-location: wmi\iwbemqualifierset.htm
tech.root: wmi
ms.assetid: 8b36bd32-4931-4641-a019-cbaa3547edd0
ms.date: 12/05/2018
ms.keywords: IWbemQualifierSet, IWbemQualifierSet interface [Windows Management Instrumentation], IWbemQualifierSet interface [Windows Management Instrumentation],described, _hmm_iwbemqualifierset, wbemcli/IWbemQualifierSet, wmi.iwbemqualifierset
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
req.dll: Fastprox.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemQualifierSet
 - wbemcli/IWbemQualifierSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
api_name:
 - IWbemQualifierSet
---

# IWbemQualifierSet interface


## -description

The 
<b>IWbemQualifierSet</b> interface acts as a container for the entire set of named qualifiers for a single property or entire object (a class or instance). The contents of the container depend on how the pointer was obtained. If the pointer was obtained from 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getqualifierset">IWbemClassObject::GetQualifierSet</a>, the object consists of the set of qualifiers for an entire object. If the pointer was obtained from 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset">IWbemClassObject::GetPropertyQualifierSet</a>, then the object represents the qualifiers for a particular property.

## -inheritance

The <b>IWbemQualifierSet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemQualifierSet</b> also has these types of members:

## -remarks

It is strongly recommended that Windows Management dynamic providers never implement this interface because  WMI provides the implementation. For more information, see 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>.

Within WMI, this interface is always in-process. Put operations only affect the local copy of the object. Get operations retrieve values from the local copy. Updates are performed only when entire objects are read or written using methods on the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface.

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>
