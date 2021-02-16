---
UID: NF:wbemprov.IWbemPropertyProvider.PutProperty
title: IWbemPropertyProvider::PutProperty (wbemprov.h)
description: The IWbemPropertyProvider::PutProperty method is called by Windows Management to update a property value supported by a property provider.
helpviewer_keywords: ["IWbemPropertyProvider interface [Windows Management Instrumentation]","PutProperty method","IWbemPropertyProvider.PutProperty","IWbemPropertyProvider::PutProperty","PutProperty","PutProperty method [Windows Management Instrumentation]","PutProperty method [Windows Management Instrumentation]","IWbemPropertyProvider interface","_hmm_iwbempropertyprovider_putproperty","wbemprov/IWbemPropertyProvider::PutProperty","wmi.iwbempropertyprovider_putproperty"]
old-location: wmi\iwbempropertyprovider_putproperty.htm
tech.root: wmi
ms.assetid: a1c25c5c-e0f9-461d-96ba-7d6d00d24d33
ms.date: 12/05/2018
ms.keywords: IWbemPropertyProvider interface [Windows Management Instrumentation],PutProperty method, IWbemPropertyProvider.PutProperty, IWbemPropertyProvider::PutProperty, PutProperty, PutProperty method [Windows Management Instrumentation], PutProperty method [Windows Management Instrumentation],IWbemPropertyProvider interface, _hmm_iwbempropertyprovider_putproperty, wbemprov/IWbemPropertyProvider::PutProperty, wmi.iwbempropertyprovider_putproperty
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
 - IWbemPropertyProvider::PutProperty
 - wbemprov/IWbemPropertyProvider::PutProperty
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
 - IWbemPropertyProvider.PutProperty
---

# IWbemPropertyProvider::PutProperty


## -description

The <b>IWbemPropertyProvider::PutProperty</b> method is called by Windows Management to update a property value supported by a property provider.

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

### -param pvValue [in]

Pointer to an existing <b>VARIANT</b> that contains the value to be written.

## -returns

This method must return <b>WBEM_S_NO_ERROR</b> if the operation succeeds, or <b>WBEM_S_FALSE</b> if the operation fails.

## -see-also

<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty">GetProperty</a>