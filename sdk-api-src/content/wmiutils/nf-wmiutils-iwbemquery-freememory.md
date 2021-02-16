---
UID: NF:wmiutils.IWbemQuery.FreeMemory
title: IWbemQuery::FreeMemory (wmiutils.h)
description: The IWbemQuery::FreeMemory method frees the memory that the parser returns to a caller in a previous call to GetAnalysis.
helpviewer_keywords: ["FreeMemory","FreeMemory method [Windows Management Instrumentation]","FreeMemory method [Windows Management Instrumentation]","IWbemQuery interface","IWbemQuery interface [Windows Management Instrumentation]","FreeMemory method","IWbemQuery.FreeMemory","IWbemQuery::FreeMemory","_hmm_iwbemquery_freememory","wmi.iwbemquery_freememory","wmiutils/IWbemQuery::FreeMemory"]
old-location: wmi\iwbemquery_freememory.htm
tech.root: wmi
ms.assetid: fbc4329d-73b8-4104-b3e0-e6dc12938b4f
ms.date: 12/05/2018
ms.keywords: FreeMemory, FreeMemory method [Windows Management Instrumentation], FreeMemory method [Windows Management Instrumentation],IWbemQuery interface, IWbemQuery interface [Windows Management Instrumentation],FreeMemory method, IWbemQuery.FreeMemory, IWbemQuery::FreeMemory, _hmm_iwbemquery_freememory, wmi.iwbemquery_freememory, wmiutils/IWbemQuery::FreeMemory
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
 - IWbemQuery::FreeMemory
 - wmiutils/IWbemQuery::FreeMemory
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
 - IWbemQuery.FreeMemory
---

# IWbemQuery::FreeMemory


## -description

The <b>IWbemQuery::FreeMemory</b> method frees the memory that the parser returns to  a caller in a previous call to 
<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">GetAnalysis</a>.

## -parameters

### -param pMem [in]

Pointer to the memory to be freed.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbemquery">IWbemQuery</a>