---
UID: NF:wmiutils.IWbemPathKeyList.SetKey
title: IWbemPathKeyList::SetKey (wmiutils.h)
description: Sets the name or value pair for a key.
helpviewer_keywords: ["IWbemPathKeyList interface [Windows Management Instrumentation]","SetKey method","IWbemPathKeyList.SetKey","IWbemPathKeyList::SetKey","SetKey","SetKey method [Windows Management Instrumentation]","SetKey method [Windows Management Instrumentation]","IWbemPathKeyList interface","_hmm_iwbempathkeylist_setkey","wmi.iwbempathkeylist_setkey","wmiutils/IWbemPathKeyList::SetKey"]
old-location: wmi\iwbempathkeylist_setkey.htm
tech.root: wmi
ms.assetid: d655c5c7-0830-46fc-a81d-9bfa16f80d68
ms.date: 12/05/2018
ms.keywords: IWbemPathKeyList interface [Windows Management Instrumentation],SetKey method, IWbemPathKeyList.SetKey, IWbemPathKeyList::SetKey, SetKey, SetKey method [Windows Management Instrumentation], SetKey method [Windows Management Instrumentation],IWbemPathKeyList interface, _hmm_iwbempathkeylist_setkey, wmi.iwbempathkeylist_setkey, wmiutils/IWbemPathKeyList::SetKey
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
 - IWbemPathKeyList::SetKey
 - wmiutils/IWbemPathKeyList::SetKey
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
 - IWbemPathKeyList.SetKey
---

# IWbemPathKeyList::SetKey


## -description

The 
<b>IWbemPathKeyList::SetKey</b> method sets the name or value pair for a key. If the key exists, it is replaced. If the name is empty, all existing keys are deleted.

## -parameters

### -param wszName [in]

Key name, may be <b>NULL</b>.

### -param uFlags [in]

Reserved. Must be 0 (zero).

### -param uCimType [in]

CIMTYPE size.

### -param pKeyVal [in]

Pointer to the data. The data pointed to varies depending on the <i>uCimType</i> parameter.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>



<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-setkey2">IWbemPathKeyList::SetKey2</a>