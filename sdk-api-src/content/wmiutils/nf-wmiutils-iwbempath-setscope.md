---
UID: NF:wmiutils.IWbemPath.SetScope
title: IWbemPath::SetScope (wmiutils.h)
description: The IWbemPath::SetScope method sets a scope in the path based upon an index. The index is always 0 (zero) and the scope is the class or key portion of the path. This method also sets the class name.
helpviewer_keywords: ["IWbemPath interface [Windows Management Instrumentation]","SetScope method","IWbemPath.SetScope","IWbemPath::SetScope","SetScope","SetScope method [Windows Management Instrumentation]","SetScope method [Windows Management Instrumentation]","IWbemPath interface","_hmm_iwbempath_setscope","wmi.iwbempath_setscope","wmiutils/IWbemPath::SetScope"]
old-location: wmi\iwbempath_setscope.htm
tech.root: wmi
ms.assetid: 0b4597ec-0d08-4929-9591-21588ded66bb
ms.date: 12/05/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],SetScope method, IWbemPath.SetScope, IWbemPath::SetScope, SetScope, SetScope method [Windows Management Instrumentation], SetScope method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_setscope, wmi.iwbempath_setscope, wmiutils/IWbemPath::SetScope
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
 - IWbemPath::SetScope
 - wmiutils/IWbemPath::SetScope
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
 - IWbemPath.SetScope
---

# IWbemPath::SetScope


## -description

The 
<b>IWbemPath::SetScope</b> method sets a scope in the path based upon an index. The index is always 0  (zero) and the scope is the class or key portion of the path. This method also sets the class name.

## -parameters

### -param uIndex [in]

Index of the scope.

### -param pszClass [in]

Class name of the scope.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>