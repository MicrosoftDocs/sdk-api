---
UID: NF:wbemcli.IWbemObjectAccess.Lock
title: IWbemObjectAccess::Lock (wbemcli.h)
description: The Lock method prevents other threads from updating an IWbemObjectAccess object until it is unlocked.
helpviewer_keywords: ["IWbemObjectAccess interface [Windows Management Instrumentation]","Lock method","IWbemObjectAccess.Lock","IWbemObjectAccess::Lock","Lock","Lock method [Windows Management Instrumentation]","Lock method [Windows Management Instrumentation]","IWbemObjectAccess interface","_hmm_iwbemobjectaccess_lock","wbemcli/IWbemObjectAccess::Lock","wmi.iwbemobjectaccess_lock"]
old-location: wmi\iwbemobjectaccess_lock.htm
tech.root: wmi
ms.assetid: c2d4f821-aa6f-48d7-8645-192afe48c30c
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],Lock method, IWbemObjectAccess.Lock, IWbemObjectAccess::Lock, Lock, Lock method [Windows Management Instrumentation], Lock method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_lock, wbemcli/IWbemObjectAccess::Lock, wmi.iwbemobjectaccess_lock
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
 - IWbemObjectAccess::Lock
 - wbemcli/IWbemObjectAccess::Lock
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
 - IWbemObjectAccess.Lock
---

# IWbemObjectAccess::Lock


## -description

The 
<b>Lock</b> method prevents other threads from updating an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a> object until it is unlocked.

## -parameters

### -param lFlags

Reserved. This parameter is currently ignored and is reserved for future use.

## -returns

This method returns <b>WBEM_S_NO_ERROR</b> if successful.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a>