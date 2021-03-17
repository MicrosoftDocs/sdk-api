---
UID: NF:wmiutils.IWbemQuery.Parse
title: IWbemQuery::Parse (wmiutils.h)
description: Parses a query string.
helpviewer_keywords: ["IWbemQuery class [Windows Management Instrumentation]","Parse method","IWbemQuery.Parse","IWbemQuery::Parse","Parse","Parse method [Windows Management Instrumentation]","Parse method [Windows Management Instrumentation]","IWbemQuery class","_hmm_iwbemquery_parse","wmi.iwbemquery_parse","wmiutils/IWbemQuery::Parse"]
old-location: wmi\iwbemquery_parse.htm
tech.root: wmi
ms.assetid: 372b004f-322e-459c-8db0-150b0483aa34
ms.date: 12/05/2018
ms.keywords: IWbemQuery class [Windows Management Instrumentation],Parse method, IWbemQuery.Parse, IWbemQuery::Parse, Parse, Parse method [Windows Management Instrumentation], Parse method [Windows Management Instrumentation],IWbemQuery class, _hmm_iwbemquery_parse, wmi.iwbemquery_parse, wmiutils/IWbemQuery::Parse
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
 - IWbemQuery::Parse
 - wmiutils/IWbemQuery::Parse
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
 - IWbemQuery.Parse
---

# IWbemQuery::Parse


## -description

The 
<b>IWbemQuery::Parse</b> method parses a query string.

## -parameters

### -param pszLang [in]

Language of the query. Must be either "WQL" or "SQL" (case-sensitive). Any other value will result in the method failing and <b>WBEM_E_INVALID_PARAMETER</b> being returned.

### -param pszQuery [in]

Valid WQL or SQL WMI query.

### -param uFlags [in]

Reserved for future use. Must be 0 (zero).

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbemquery">IWbemQuery</a>