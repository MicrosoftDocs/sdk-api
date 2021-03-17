---
UID: NF:wmiutils.IWbemPathKeyList.SetKey2
title: IWbemPathKeyList::SetKey2 (wmiutils.h)
description: Sets the name or value pair for a key using variants.
helpviewer_keywords: ["IWbemPathKeyList interface [Windows Management Instrumentation]","SetKey2 method","IWbemPathKeyList.SetKey2","IWbemPathKeyList::SetKey2","SetKey2","SetKey2 method [Windows Management Instrumentation]","SetKey2 method [Windows Management Instrumentation]","IWbemPathKeyList interface","_hmm_iwbempathkeylist_setkey2","wmi.iwbempathkeylist_setkey2","wmiutils/IWbemPathKeyList::SetKey2"]
old-location: wmi\iwbempathkeylist_setkey2.htm
tech.root: wmi
ms.assetid: 3b282124-d544-405a-96e0-39cc504c8117
ms.date: 12/05/2018
ms.keywords: IWbemPathKeyList interface [Windows Management Instrumentation],SetKey2 method, IWbemPathKeyList.SetKey2, IWbemPathKeyList::SetKey2, SetKey2, SetKey2 method [Windows Management Instrumentation], SetKey2 method [Windows Management Instrumentation],IWbemPathKeyList interface, _hmm_iwbempathkeylist_setkey2, wmi.iwbempathkeylist_setkey2, wmiutils/IWbemPathKeyList::SetKey2
req.header: wmiutils.h
req.include-header: 
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
req.dll: Wmiutils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemPathKeyList::SetKey2
 - wmiutils/IWbemPathKeyList::SetKey2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPathKeyList.SetKey2
---

# IWbemPathKeyList::SetKey2


## -description

The 
<b>IWbemPathKeyList::SetKey2</b> method sets the name or value pair for a key using variants. If the key exists, it is replaced.

## -parameters

### -param wszName [in]

Key name, may be <b>NULL</b>.

### -param uFlags [in]

Reserved. Must be 0 (zero).

### -param uCimType [in]

CIMTYPE size.

### -param pKeyVal [in]

Pointer to a variant that contains the data.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>