---
UID: NF:wmiutils.IWbemPathKeyList.RemoveKey
title: IWbemPathKeyList::RemoveKey (wmiutils.h)
description: The IWbemPathKeyList::RemoveKey method removes the key that matches the wszName parameter.
helpviewer_keywords: ["IWbemPathKeyList interface [Windows Management Instrumentation]","RemoveKey method","IWbemPathKeyList.RemoveKey","IWbemPathKeyList::RemoveKey","RemoveKey","RemoveKey method [Windows Management Instrumentation]","RemoveKey method [Windows Management Instrumentation]","IWbemPathKeyList interface","_hmm_iwbempathkeylist_removekey","wmi.iwbempathkeylist_removekey","wmiutils/IWbemPathKeyList::RemoveKey"]
old-location: wmi\iwbempathkeylist_removekey.htm
tech.root: wmi
ms.assetid: 07166023-2945-49d5-9d2d-8cac12053ed9
ms.date: 12/05/2018
ms.keywords: IWbemPathKeyList interface [Windows Management Instrumentation],RemoveKey method, IWbemPathKeyList.RemoveKey, IWbemPathKeyList::RemoveKey, RemoveKey, RemoveKey method [Windows Management Instrumentation], RemoveKey method [Windows Management Instrumentation],IWbemPathKeyList interface, _hmm_iwbempathkeylist_removekey, wmi.iwbempathkeylist_removekey, wmiutils/IWbemPathKeyList::RemoveKey
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
 - IWbemPathKeyList::RemoveKey
 - wmiutils/IWbemPathKeyList::RemoveKey
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
 - IWbemPathKeyList.RemoveKey
---

# IWbemPathKeyList::RemoveKey


## -description

The 
<b>IWbemPathKeyList::RemoveKey</b> method removes the key that matches the <i>wszName</i> parameter.

## -parameters

### -param wszName [in, out]

Name of the key to be removed.

### -param uFlags [in]

Reserved. Must be 0 (zero).

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>



<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-removeallkeys">IWbemPathKeyList::RemoveAllKeys</a>