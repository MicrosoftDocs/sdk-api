---
UID: NF:wbemcli.IWbemObjectAccess.WriteQWORD
title: IWbemObjectAccess::WriteQWORD (wbemcli.h)
description: The WriteQWORD method writes 64 bits of data to a property by using a property handle.
helpviewer_keywords: ["IWbemObjectAccess interface [Windows Management Instrumentation]","WriteQWORD method","IWbemObjectAccess.WriteQWORD","IWbemObjectAccess::WriteQWORD","WriteQWORD","WriteQWORD method [Windows Management Instrumentation]","WriteQWORD method [Windows Management Instrumentation]","IWbemObjectAccess interface","_hmm_iwbemobjectaccess_writeqword","wbemcli/IWbemObjectAccess::WriteQWORD","wmi.iwbemobjectaccess_writeqword"]
old-location: wmi\iwbemobjectaccess_writeqword.htm
tech.root: wmi
ms.assetid: f0d098b7-06f4-4a0a-8db9-fa1ef9be4468
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],WriteQWORD method, IWbemObjectAccess.WriteQWORD, IWbemObjectAccess::WriteQWORD, WriteQWORD, WriteQWORD method [Windows Management Instrumentation], WriteQWORD method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_writeqword, wbemcli/IWbemObjectAccess::WriteQWORD, wmi.iwbemobjectaccess_writeqword
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
 - IWbemObjectAccess::WriteQWORD
 - wbemcli/IWbemObjectAccess::WriteQWORD
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
 - IWbemObjectAccess.WriteQWORD
---

# IWbemObjectAccess::WriteQWORD


## -description

The <b>WriteQWORD</b> method writes 64 bits of data to a property by using a property handle.

## -parameters

### -param lHandle [in]

Integer that contains the handle that identifies this property.

### -param pw [in]

Unsigned 64-bit integer that contains the data written to the specified property.

## -returns

This method returns <b>WBEM_S_NO_ERROR</b> if successful.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>