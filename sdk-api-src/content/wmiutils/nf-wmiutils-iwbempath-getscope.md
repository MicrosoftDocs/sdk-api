---
UID: NF:wmiutils.IWbemPath.GetScope
title: IWbemPath::GetScope (wmiutils.h)
description: Retrieves a scope based upon an index.
helpviewer_keywords: ["GetScope","GetScope method [Windows Management Instrumentation]","GetScope method [Windows Management Instrumentation]","IWbemPath interface","IWbemPath interface [Windows Management Instrumentation]","GetScope method","IWbemPath.GetScope","IWbemPath::GetScope","_hmm_iwbempath_getscope","wmi.iwbempath_getscope","wmiutils/IWbemPath::GetScope"]
old-location: wmi\iwbempath_getscope.htm
tech.root: wmi
ms.assetid: 9601fb2b-583d-4481-8237-32db72432c63
ms.date: 12/05/2018
ms.keywords: GetScope, GetScope method [Windows Management Instrumentation], GetScope method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetScope method, IWbemPath.GetScope, IWbemPath::GetScope, _hmm_iwbempath_getscope, wmi.iwbempath_getscope, wmiutils/IWbemPath::GetScope
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
 - IWbemPath::GetScope
 - wmiutils/IWbemPath::GetScope
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
 - IWbemPath.GetScope
---

# IWbemPath::GetScope


## -description

The 
<b>IWbemPath::GetScope</b> method retrieves a scope based upon an index. This method retrieves the class name and a 
<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a> pointer so that the details of the keys can be retrieved.

## -parameters

### -param uIndex [in]

Index of the scope.

### -param puClassNameBufSize [in, out]

Caller sets this to the number of characters that the buffer can hold. Upon success, this is set to the number of characters copied into the buffer including the <b>NULL</b> terminator.

### -param pszClass [out]

Buffer where the scope is to be copied.

### -param pKeyList [out]

Pointer to an 
<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a> object.

## -returns

This method returns the following values.

## -remarks

This method can be used to determine how big a buffer is needed for <i>pszClass</i>. This is done by passing in a <b>NULL</b> pointer for the buffer, setting <i>puClassNameBufSize</i> to 0 and then making the call. Upon return, <i>puClassNameBufSize</i> indicates how large of a buffer is needed for <i>pszClass</i> and its terminating <b>NULL</b> character.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>