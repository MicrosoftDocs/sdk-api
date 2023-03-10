---
UID: NF:wbemcli.IWbemObjectAccess.GetPropertyInfoByHandle
title: IWbemObjectAccess::GetPropertyInfoByHandle (wbemcli.h)
description: The GetPropertyInfoByHandle method returns the name and data type of the property that is associated with a property handle.
helpviewer_keywords: ["GetPropertyInfoByHandle","GetPropertyInfoByHandle method [Windows Management Instrumentation]","GetPropertyInfoByHandle method [Windows Management Instrumentation]","IWbemObjectAccess interface","IWbemObjectAccess interface [Windows Management Instrumentation]","GetPropertyInfoByHandle method","IWbemObjectAccess.GetPropertyInfoByHandle","IWbemObjectAccess::GetPropertyInfoByHandle","_hmm_iwbemobjectaccess_getpropertyinfobyhandle","wbemcli/IWbemObjectAccess::GetPropertyInfoByHandle","wmi.iwbemobjectaccess_getpropertyinfobyhandle"]
old-location: wmi\iwbemobjectaccess_getpropertyinfobyhandle.htm
tech.root: wmi
ms.assetid: a29157a8-50da-485d-a2b1-bf9645ba9963
ms.date: 12/05/2018
ms.keywords: GetPropertyInfoByHandle, GetPropertyInfoByHandle method [Windows Management Instrumentation], GetPropertyInfoByHandle method [Windows Management Instrumentation],IWbemObjectAccess interface, IWbemObjectAccess interface [Windows Management Instrumentation],GetPropertyInfoByHandle method, IWbemObjectAccess.GetPropertyInfoByHandle, IWbemObjectAccess::GetPropertyInfoByHandle, _hmm_iwbemobjectaccess_getpropertyinfobyhandle, wbemcli/IWbemObjectAccess::GetPropertyInfoByHandle, wmi.iwbemobjectaccess_getpropertyinfobyhandle
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
 - IWbemObjectAccess::GetPropertyInfoByHandle
 - wbemcli/IWbemObjectAccess::GetPropertyInfoByHandle
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
 - IWbemObjectAccess.GetPropertyInfoByHandle
---

# IWbemObjectAccess::GetPropertyInfoByHandle


## -description

The 
<b>GetPropertyInfoByHandle</b> method returns the name and data type of the property that is associated with a property handle.

## -parameters

### -param lHandle [in]

Integer that contains the handle identifying the property.

### -param pstrName [out]

Pointer to a string used to return the name of the specified property.

### -param pType [out]

Pointer to a <b>CIMTYPE</b> used to return the type of the property.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>