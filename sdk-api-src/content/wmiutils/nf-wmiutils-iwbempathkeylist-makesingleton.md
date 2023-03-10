---
UID: NF:wmiutils.IWbemPathKeyList.MakeSingleton
title: IWbemPathKeyList::MakeSingleton (wmiutils.h)
description: The IWbemPathKeyList::MakeSingleton method governs whether or not a key is singleton.
helpviewer_keywords: ["IWbemPathKeyList interface [Windows Management Instrumentation]","MakeSingleton method","IWbemPathKeyList.MakeSingleton","IWbemPathKeyList::MakeSingleton","MakeSingleton","MakeSingleton method [Windows Management Instrumentation]","MakeSingleton method [Windows Management Instrumentation]","IWbemPathKeyList interface","_hmm_iwbempathkeylist_makesingleton","wmi.iwbempathkeylist_makesingleton","wmiutils/IWbemPathKeyList::MakeSingleton"]
old-location: wmi\iwbempathkeylist_makesingleton.htm
tech.root: wmi
ms.assetid: 6dd7fd31-126c-4702-8e43-3e6b08912b30
ms.date: 12/05/2018
ms.keywords: IWbemPathKeyList interface [Windows Management Instrumentation],MakeSingleton method, IWbemPathKeyList.MakeSingleton, IWbemPathKeyList::MakeSingleton, MakeSingleton, MakeSingleton method [Windows Management Instrumentation], MakeSingleton method [Windows Management Instrumentation],IWbemPathKeyList interface, _hmm_iwbempathkeylist_makesingleton, wmi.iwbempathkeylist_makesingleton, wmiutils/IWbemPathKeyList::MakeSingleton
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
 - IWbemPathKeyList::MakeSingleton
 - wmiutils/IWbemPathKeyList::MakeSingleton
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
 - IWbemPathKeyList.MakeSingleton
---

# IWbemPathKeyList::MakeSingleton


## -description

The 
<b>IWbemPathKeyList::MakeSingleton</b> method governs whether or not a key is singleton.

## -parameters

### -param bSet [in]

If <b>TRUE</b>, the key becomes singleton. If <b>FALSE</b>, the key is no longer singleton.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>