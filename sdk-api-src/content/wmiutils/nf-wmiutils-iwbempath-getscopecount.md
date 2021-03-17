---
UID: NF:wmiutils.IWbemPath.GetScopeCount
title: IWbemPath::GetScopeCount (wmiutils.h)
description: The IWbemPath::GetScopeCount method returns the number of scopes in the path.
helpviewer_keywords: ["GetScopeCount","GetScopeCount method [Windows Management Instrumentation]","GetScopeCount method [Windows Management Instrumentation]","IWbemPath interface","IWbemPath interface [Windows Management Instrumentation]","GetScopeCount method","IWbemPath.GetScopeCount","IWbemPath::GetScopeCount","_hmm_iwbempath_getscopecount","wmi.iwbempath_getscopecount","wmiutils/IWbemPath::GetScopeCount"]
old-location: wmi\iwbempath_getscopecount.htm
tech.root: wmi
ms.assetid: 3e818a4d-0a38-44ce-9027-2a94b7c86bef
ms.date: 12/05/2018
ms.keywords: GetScopeCount, GetScopeCount method [Windows Management Instrumentation], GetScopeCount method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetScopeCount method, IWbemPath.GetScopeCount, IWbemPath::GetScopeCount, _hmm_iwbempath_getscopecount, wmi.iwbempath_getscopecount, wmiutils/IWbemPath::GetScopeCount
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
 - IWbemPath::GetScopeCount
 - wmiutils/IWbemPath::GetScopeCount
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
 - IWbemPath.GetScopeCount
---

# IWbemPath::GetScopeCount


## -description

The <b>IWbemPath::GetScopeCount</b> method returns the 
    number of scopes in the path.

## -parameters

### -param puCount [out]

Number of scopes in the path. When there is a scope it is basically the class or key portion of the path.

## -returns

This method returns the following values.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>