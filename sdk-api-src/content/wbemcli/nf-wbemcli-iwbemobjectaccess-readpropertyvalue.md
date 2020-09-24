---
UID: NF:wbemcli.IWbemObjectAccess.ReadPropertyValue
title: IWbemObjectAccess::ReadPropertyValue (wbemcli.h)
description: The ReadPropertyValue method returns a specified number of bytes of a property associated with a property handle.
helpviewer_keywords: ["IWbemObjectAccess interface [Windows Management Instrumentation]","ReadPropertyValue method","IWbemObjectAccess.ReadPropertyValue","IWbemObjectAccess::ReadPropertyValue","ReadPropertyValue","ReadPropertyValue method [Windows Management Instrumentation]","ReadPropertyValue method [Windows Management Instrumentation]","IWbemObjectAccess interface","_hmm_iwbemobjectaccess_readpropertyvalue","wbemcli/IWbemObjectAccess::ReadPropertyValue","wmi.iwbemobjectaccess_readpropertyvalue"]
old-location: wmi\iwbemobjectaccess_readpropertyvalue.htm
tech.root: wmi
ms.assetid: 878fa803-73dc-45ad-8d58-2decb7e316b2
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],ReadPropertyValue method, IWbemObjectAccess.ReadPropertyValue, IWbemObjectAccess::ReadPropertyValue, ReadPropertyValue, ReadPropertyValue method [Windows Management Instrumentation], ReadPropertyValue method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_readpropertyvalue, wbemcli/IWbemObjectAccess::ReadPropertyValue, wmi.iwbemobjectaccess_readpropertyvalue
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
 - IWbemObjectAccess::ReadPropertyValue
 - wbemcli/IWbemObjectAccess::ReadPropertyValue
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
 - IWbemObjectAccess.ReadPropertyValue
---

# IWbemObjectAccess::ReadPropertyValue


## -description

The <b>ReadPropertyValue</b> method returns a specified number of bytes of a property associated with a property handle. Use this method to read the value of a property that contains a string or to read a property that contains a value that is not 32 (<b>DWORD</b>) or 64 (<b>QWORD</b>) bits long.

## -parameters

### -param lHandle [in]

Integer that contains the handle identifying this property.

### -param lBufferSize [in]

Integer that contains the buffer size.

### -param plNumBytes [out]

Pointer to an integer used to return the number of bytes read.

### -param aData [out]

Pointer to an array used to return the property data.

## -returns

This method returns <b>WBEM_S_NO_ERROR</b> if successful; otherwise, this method returns an <b>HRESULT</b> with one of the following values.

## -remarks

String data is returned as <b>null</b>-terminated <b>WCHAR</b> data.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>