---
UID: NF:wbemprov.IWbemPropertyProvider.GetProperty
title: IWbemPropertyProvider::GetProperty (wbemprov.h)
description: The IWbemPropertyProvider::GetProperty method is called by Windows Management to retrieve an individual property value.
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Management Instrumentation]","GetProperty method [Windows Management Instrumentation]","IWbemPropertyProvider interface","IWbemPropertyProvider interface [Windows Management Instrumentation]","GetProperty method","IWbemPropertyProvider.GetProperty","IWbemPropertyProvider::GetProperty","_hmm_iwbempropertyprovider_getproperty","wbemprov/IWbemPropertyProvider::GetProperty","wmi.iwbempropertyprovider_getproperty"]
old-location: wmi\iwbempropertyprovider_getproperty.htm
tech.root: wmi
ms.assetid: 6ee0e904-7f4c-4b32-8a90-d727340b481e
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Management Instrumentation], GetProperty method [Windows Management Instrumentation],IWbemPropertyProvider interface, IWbemPropertyProvider interface [Windows Management Instrumentation],GetProperty method, IWbemPropertyProvider.GetProperty, IWbemPropertyProvider::GetProperty, _hmm_iwbempropertyprovider_getproperty, wbemprov/IWbemPropertyProvider::GetProperty, wmi.iwbempropertyprovider_getproperty
req.header: wbemprov.h
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
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemPropertyProvider::GetProperty
 - wbemprov/IWbemPropertyProvider::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemPropertyProvider.GetProperty
---

# IWbemPropertyProvider::GetProperty


## -description

The 
<b>IWbemPropertyProvider::GetProperty</b> method is called by Windows Management to retrieve an individual property value.

## -parameters

### -param lFlags [in]

Reserved. This parameter must be 0.

### -param strLocale [in]

String indicating the desired locale in cases where the returned property value can be localized. If the property cannot be localized, the implementation can ignore this value.

### -param strClassMapping [in]

Literal copy of the string value for the <b>ClassContext</b> qualifier for the class. This points to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.

### -param strInstMapping [in]

Literal copy of the string value for the <b>InstanceContext</b> qualifier for the instance. This must point to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.

### -param strPropMapping [in]

Literal copy of the value of the <b>PropertyContext</b> qualifier for the property. This must point to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.

### -param pvValue [out]

Pointer to an uninitialized <b>VARIANT</b> that receives the value for the property. The implementation must call <b>VariantInit</b> and return the value. If an error occurs, the implementation is expected to ignore the pointer.

## -returns

This method must return <b>WBEM_S_NO_ERROR</b> if the call succeeds. If the call fails, the method must return <b>WBEM_S_FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty">Constructing Property Providers</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbempropertyprovider">IWbemPropertyProvider</a>



<b>PutProperty</b>