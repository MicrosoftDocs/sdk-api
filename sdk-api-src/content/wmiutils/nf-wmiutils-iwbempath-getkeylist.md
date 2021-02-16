---
UID: NF:wmiutils.IWbemPath.GetKeyList
title: IWbemPath::GetKeyList (wmiutils.h)
description: Retrieves an IWbemPathKeyList pointer so that the individual key may be accessed.
helpviewer_keywords: ["GetKeyList","GetKeyList method [Windows Management Instrumentation]","GetKeyList method [Windows Management Instrumentation]","IWbemPath interface","IWbemPath interface [Windows Management Instrumentation]","GetKeyList method","IWbemPath.GetKeyList","IWbemPath::GetKeyList","_hmm_iwbempath_getkeylist","wmi.iwbempath_getkeylist","wmiutils/IWbemPath::GetKeyList"]
old-location: wmi\iwbempath_getkeylist.htm
tech.root: wmi
ms.assetid: bf62727f-6ce7-4c7a-b757-c36d8cf64652
ms.date: 12/05/2018
ms.keywords: GetKeyList, GetKeyList method [Windows Management Instrumentation], GetKeyList method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetKeyList method, IWbemPath.GetKeyList, IWbemPath::GetKeyList, _hmm_iwbempath_getkeylist, wmi.iwbempath_getkeylist, wmiutils/IWbemPath::GetKeyList
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
 - IWbemPath::GetKeyList
 - wmiutils/IWbemPath::GetKeyList
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
 - IWbemPath.GetKeyList
---

# IWbemPath::GetKeyList


## -description

The 
<b>IWbemPath::GetKeyList</b> method retrieves an 
<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a> pointer so that the individual key may be accessed.

## -parameters

### -param pOut [out]

Pointer to an 
<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a> object.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>