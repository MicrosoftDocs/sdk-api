---
UID: NF:wbemcli.IWbemObjectAccess.ReadDWORD
title: IWbemObjectAccess::ReadDWORD (wbemcli.h)
description: The ReadDWORD method reads 32 bits of property data using a property handle.
helpviewer_keywords: ["IWbemObjectAccess interface [Windows Management Instrumentation]","ReadDWORD method","IWbemObjectAccess.ReadDWORD","IWbemObjectAccess::ReadDWORD","ReadDWORD","ReadDWORD method [Windows Management Instrumentation]","ReadDWORD method [Windows Management Instrumentation]","IWbemObjectAccess interface","_hmm_iwbemobjectaccess_readdword","wbemcli/IWbemObjectAccess::ReadDWORD","wmi.iwbemobjectaccess_readdword"]
old-location: wmi\iwbemobjectaccess_readdword.htm
tech.root: wmi
ms.assetid: 5352dea3-6d10-42be-aa1e-786ace193827
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],ReadDWORD method, IWbemObjectAccess.ReadDWORD, IWbemObjectAccess::ReadDWORD, ReadDWORD, ReadDWORD method [Windows Management Instrumentation], ReadDWORD method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_readdword, wbemcli/IWbemObjectAccess::ReadDWORD, wmi.iwbemobjectaccess_readdword
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
 - IWbemObjectAccess::ReadDWORD
 - wbemcli/IWbemObjectAccess::ReadDWORD
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
 - IWbemObjectAccess.ReadDWORD
---

# IWbemObjectAccess::ReadDWORD


## -description

The <b>ReadDWORD</b> method reads 32 bits of property data using a property handle.

## -parameters

### -param lHandle [in]

Integer that contains the handle that identifies this property.

### -param pdw [out]

Pointer to a 32-bit unsigned integer used to return the data.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>