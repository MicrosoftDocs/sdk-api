---
UID: NF:wbemcli.IWbemObjectAccess.Unlock
title: IWbemObjectAccess::Unlock (wbemcli.h)
description: The Unlock method allows other threads to update the property values of an IWbemObjectAccess object.
helpviewer_keywords: ["IWbemObjectAccess interface [Windows Management Instrumentation]","Unlock method","IWbemObjectAccess.Unlock","IWbemObjectAccess::Unlock","Unlock","Unlock method [Windows Management Instrumentation]","Unlock method [Windows Management Instrumentation]","IWbemObjectAccess interface","_hmm_iwbemobjectaccess_unlock","wbemcli/IWbemObjectAccess::Unlock","wmi.iwbemobjectaccess_unlock"]
old-location: wmi\iwbemobjectaccess_unlock.htm
tech.root: wmi
ms.assetid: a1b841b2-684e-4697-b802-b0534f752a13
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],Unlock method, IWbemObjectAccess.Unlock, IWbemObjectAccess::Unlock, Unlock, Unlock method [Windows Management Instrumentation], Unlock method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_unlock, wbemcli/IWbemObjectAccess::Unlock, wmi.iwbemobjectaccess_unlock
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
 - IWbemObjectAccess::Unlock
 - wbemcli/IWbemObjectAccess::Unlock
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
 - IWbemObjectAccess.Unlock
---

# IWbemObjectAccess::Unlock


## -description

The <b>Unlock</b> method allows other threads to update the property values of an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a> object.

## -parameters

### -param lFlags

Reserved. This parameter is currently ignored and is reserved for future use.

## -returns

This method returns <b>WBEM_S_NO_ERROR</b> if successful.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>