---
UID: NF:wbemcli.IWbemObjectAccess.WriteDWORD
title: IWbemObjectAccess::WriteDWORD (wbemcli.h)
description: The WriteDWORD method writes 32 bits of data to a property identified by a property handle.
helpviewer_keywords: ["IWbemObjectAccess interface [Windows Management Instrumentation]","WriteDWORD method","IWbemObjectAccess.WriteDWORD","IWbemObjectAccess::WriteDWORD","WriteDWORD","WriteDWORD method [Windows Management Instrumentation]","WriteDWORD method [Windows Management Instrumentation]","IWbemObjectAccess interface","_hmm_iwbemobjectaccess_writedword","wbemcli/IWbemObjectAccess::WriteDWORD","wmi.iwbemobjectaccess_writedword"]
old-location: wmi\iwbemobjectaccess_writedword.htm
tech.root: wmi
ms.assetid: a1716599-69ba-44fb-be68-b22578f6c6b2
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],WriteDWORD method, IWbemObjectAccess.WriteDWORD, IWbemObjectAccess::WriteDWORD, WriteDWORD, WriteDWORD method [Windows Management Instrumentation], WriteDWORD method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_writedword, wbemcli/IWbemObjectAccess::WriteDWORD, wmi.iwbemobjectaccess_writedword
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
 - IWbemObjectAccess::WriteDWORD
 - wbemcli/IWbemObjectAccess::WriteDWORD
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
 - IWbemObjectAccess.WriteDWORD
---

# IWbemObjectAccess::WriteDWORD


## -description

The <b>WriteDWORD</b> method writes 32 bits of data to a property identified by a property handle.

## -parameters

### -param lHandle [in]

Integer that contains the handle identifying this property.

### -param dw [in]

Unsigned 32-bit integer that contains the data being written.

## -returns

This method returns <b>WBEM_S_NO_ERROR</b> if successful.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>