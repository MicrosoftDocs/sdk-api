---
UID: NF:wbemcli.IWbemObjectAccess.ReadQWORD
title: IWbemObjectAccess::ReadQWORD (wbemcli.h)
description: The ReadQWORD method reads 64 bits of property data identified by a property handle.
helpviewer_keywords: ["IWbemObjectAccess interface [Windows Management Instrumentation]","ReadQWORD method","IWbemObjectAccess.ReadQWORD","IWbemObjectAccess::ReadQWORD","ReadQWORD","ReadQWORD method [Windows Management Instrumentation]","ReadQWORD method [Windows Management Instrumentation]","IWbemObjectAccess interface","_hmm_iwbemobjectaccess_readqword","wbemcli/IWbemObjectAccess::ReadQWORD","wmi.iwbemobjectaccess_readqword"]
old-location: wmi\iwbemobjectaccess_readqword.htm
tech.root: wmi
ms.assetid: cb76eb26-e407-411a-9ccb-a03eaa8bf22e
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],ReadQWORD method, IWbemObjectAccess.ReadQWORD, IWbemObjectAccess::ReadQWORD, ReadQWORD, ReadQWORD method [Windows Management Instrumentation], ReadQWORD method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_readqword, wbemcli/IWbemObjectAccess::ReadQWORD, wmi.iwbemobjectaccess_readqword
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
 - IWbemObjectAccess::ReadQWORD
 - wbemcli/IWbemObjectAccess::ReadQWORD
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
 - IWbemObjectAccess.ReadQWORD
---

# IWbemObjectAccess::ReadQWORD


## -description

The <b>ReadQWORD</b> method reads 64 bits of property data identified by a property handle.

## -parameters

### -param lHandle [in]

Integer that contains the handle identifying the property.

### -param pqw [out]

Pointer to a unsigned 64-bit integer used to return the data being read.

## -returns

This method returns <b>WBEM_S_NO_ERROR</b> if successful. If the property was <b>NULL</b>, then the method returns <b>WBEM_S_FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>