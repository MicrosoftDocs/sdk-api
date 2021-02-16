---
UID: NF:wmiutils.IWbemPath.GetNamespaceAt
title: IWbemPath::GetNamespaceAt (wmiutils.h)
description: Retrieves a namespace based upon its index.
helpviewer_keywords: ["GetNamespaceAt","GetNamespaceAt method [Windows Management Instrumentation]","GetNamespaceAt method [Windows Management Instrumentation]","IWbemPath interface","IWbemPath interface [Windows Management Instrumentation]","GetNamespaceAt method","IWbemPath.GetNamespaceAt","IWbemPath::GetNamespaceAt","_hmm_iwbempath_getnamespaceat","wmi.iwbempath_getnamespaceat","wmiutils/IWbemPath::GetNamespaceAt"]
old-location: wmi\iwbempath_getnamespaceat.htm
tech.root: wmi
ms.assetid: a5180c35-df90-447d-ad52-250ececfd525
ms.date: 12/05/2018
ms.keywords: GetNamespaceAt, GetNamespaceAt method [Windows Management Instrumentation], GetNamespaceAt method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetNamespaceAt method, IWbemPath.GetNamespaceAt, IWbemPath::GetNamespaceAt, _hmm_iwbempath_getnamespaceat, wmi.iwbempath_getnamespaceat, wmiutils/IWbemPath::GetNamespaceAt
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
 - IWbemPath::GetNamespaceAt
 - wmiutils/IWbemPath::GetNamespaceAt
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
 - IWbemPath.GetNamespaceAt
---

# IWbemPath::GetNamespaceAt


## -description

The 
<b>IWbemPath::GetNamespaceAt</b> method retrieves a namespace based upon its index. The leftmost namespace in the path has an index of 0 with each namespace moving to the right having a progressively higher index value.

## -parameters

### -param uIndex [in]

Index of the namespace to be read. The leftmost namespace in the path is index 0 with each namespace to the right having a progressively higher index value. The maximum permitted value is one less than the current number of namespaces.

### -param puNameBufLength [in, out]

Caller sets this to the number of characters the buffer can hold. Upon success, this is set to the number of characters copied into the buffer including the <b>NULL</b> terminator.

### -param pName [in, out]

Namespace name.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -remarks

This method can be used to determine how big a buffer is needed for <i>pName</i>. This is done by passing in a <b>NULL</b> pointer for the buffer, setting <i>puNameBufLength</i> to 0 and then making the call. Upon return, <i>puNameBufLength</i> indicates how large of a buffer is needed for <i>pName</i> and its terminating <b>NULL</b> character.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>