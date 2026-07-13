---
UID: NF:mfidl.IMFNetProxyLocator.FindNextProxy
title: IMFNetProxyLocator::FindNextProxy (mfidl.h)
description: Determines the next proxy to use.
helpviewer_keywords: ["91a6046f-f5c3-4239-af71-d25e9d5b5838","FindNextProxy","FindNextProxy method [Media Foundation]","FindNextProxy method [Media Foundation]","IMFNetProxyLocator interface","IMFNetProxyLocator interface [Media Foundation]","FindNextProxy method","IMFNetProxyLocator.FindNextProxy","IMFNetProxyLocator::FindNextProxy","mf.imfnetproxylocator_findnextproxy","mfidl/IMFNetProxyLocator::FindNextProxy"]
old-location: mf\imfnetproxylocator_findnextproxy.htm
tech.root: mf
ms.assetid: 91a6046f-f5c3-4239-af71-d25e9d5b5838
ms.date: 12/05/2018
ms.keywords: 91a6046f-f5c3-4239-af71-d25e9d5b5838, FindNextProxy, FindNextProxy method [Media Foundation], FindNextProxy method [Media Foundation],IMFNetProxyLocator interface, IMFNetProxyLocator interface [Media Foundation],FindNextProxy method, IMFNetProxyLocator.FindNextProxy, IMFNetProxyLocator::FindNextProxy, mf.imfnetproxylocator_findnextproxy, mfidl/IMFNetProxyLocator::FindNextProxy
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
 - IMFNetProxyLocator::FindNextProxy
 - mfidl/IMFNetProxyLocator::FindNextProxy
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
 - IMFNetProxyLocator.FindNextProxy
---

# IMFNetProxyLocator::FindNextProxy


## -description

Determines the next proxy to use.



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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more proxy objects.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator">IMFNetProxyLocator</a>
