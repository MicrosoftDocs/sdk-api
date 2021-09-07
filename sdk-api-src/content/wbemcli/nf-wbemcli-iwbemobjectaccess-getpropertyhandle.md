---
UID: NF:wbemcli.IWbemObjectAccess.GetPropertyHandle
title: IWbemObjectAccess::GetPropertyHandle (wbemcli.h)
description: The GetPropertyHandle method returns a unique handle that identifies a property. You can use this handle to identify properties when using IWbemObjectAccess methods to read or write property values.
helpviewer_keywords: ["GetPropertyHandle","GetPropertyHandle method [Windows Management Instrumentation]","GetPropertyHandle method [Windows Management Instrumentation]","IWbemObjectAccess interface","IWbemObjectAccess interface [Windows Management Instrumentation]","GetPropertyHandle method","IWbemObjectAccess.GetPropertyHandle","IWbemObjectAccess::GetPropertyHandle","_hmm_iwbemobjectaccess_getpropertyhandle","wbemcli/IWbemObjectAccess::GetPropertyHandle","wmi.iwbemobjectaccess_getpropertyhandle"]
old-location: wmi\iwbemobjectaccess_getpropertyhandle.htm
tech.root: wmi
ms.assetid: 889d90cd-f53f-460e-b1c2-ed2b87863d58
ms.date: 12/05/2018
ms.keywords: GetPropertyHandle, GetPropertyHandle method [Windows Management Instrumentation], GetPropertyHandle method [Windows Management Instrumentation],IWbemObjectAccess interface, IWbemObjectAccess interface [Windows Management Instrumentation],GetPropertyHandle method, IWbemObjectAccess.GetPropertyHandle, IWbemObjectAccess::GetPropertyHandle, _hmm_iwbemobjectaccess_getpropertyhandle, wbemcli/IWbemObjectAccess::GetPropertyHandle, wmi.iwbemobjectaccess_getpropertyhandle
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
 - IWbemObjectAccess::GetPropertyHandle
 - wbemcli/IWbemObjectAccess::GetPropertyHandle
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
 - IWbemObjectAccess.GetPropertyHandle
---

# IWbemObjectAccess::GetPropertyHandle


## -description

The 
<b>GetPropertyHandle</b> method returns a unique handle that identifies a property. You can use this handle to identify properties when using 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a> methods to read or write property values.

## -parameters

### -param wszPropertyName [in]

Constant, null-terminated string of 16-bit Unicode characters that contains the property name.

### -param pType [out]

Pointer to a <b>CIMTYPE</b> used to return the CIM type of the property.

### -param plHandle [out]

Pointer to an integer used to return the property handle.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

Handles can be retrieved for all data types other than CIM_OBJECT and CIM_ARRAY. Returned handles work across all instances of a class.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>