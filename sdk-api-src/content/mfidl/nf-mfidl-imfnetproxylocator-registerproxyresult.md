---
UID: NF:mfidl.IMFNetProxyLocator.RegisterProxyResult
title: IMFNetProxyLocator::RegisterProxyResult (mfidl.h)
description: Keeps a record of the success or failure of using the current proxy.
helpviewer_keywords: ["2b1a55c6-7d78-47cc-9098-6504d11a4eef","IMFNetProxyLocator interface [Media Foundation]","RegisterProxyResult method","IMFNetProxyLocator.RegisterProxyResult","IMFNetProxyLocator::RegisterProxyResult","RegisterProxyResult","RegisterProxyResult method [Media Foundation]","RegisterProxyResult method [Media Foundation]","IMFNetProxyLocator interface","mf.imfnetproxylocator_registerproxyresult","mfidl/IMFNetProxyLocator::RegisterProxyResult"]
old-location: mf\imfnetproxylocator_registerproxyresult.htm
tech.root: mf
ms.assetid: 2b1a55c6-7d78-47cc-9098-6504d11a4eef
ms.date: 12/05/2018
ms.keywords: 2b1a55c6-7d78-47cc-9098-6504d11a4eef, IMFNetProxyLocator interface [Media Foundation],RegisterProxyResult method, IMFNetProxyLocator.RegisterProxyResult, IMFNetProxyLocator::RegisterProxyResult, RegisterProxyResult, RegisterProxyResult method [Media Foundation], RegisterProxyResult method [Media Foundation],IMFNetProxyLocator interface, mf.imfnetproxylocator_registerproxyresult, mfidl/IMFNetProxyLocator::RegisterProxyResult
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetProxyLocator::RegisterProxyResult
 - mfidl/IMFNetProxyLocator::RegisterProxyResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetProxyLocator.RegisterProxyResult
---

# IMFNetProxyLocator::RegisterProxyResult


## -description

Keeps a record of the success or failure of using the current proxy.

## -parameters

### -param hrOp [in]

<b>HRESULT</b> specifying the result of using the current proxy for connection.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator">IMFNetProxyLocator</a>