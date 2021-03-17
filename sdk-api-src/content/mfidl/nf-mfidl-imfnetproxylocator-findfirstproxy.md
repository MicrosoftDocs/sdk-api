---
UID: NF:mfidl.IMFNetProxyLocator.FindFirstProxy
title: IMFNetProxyLocator::FindFirstProxy (mfidl.h)
description: Initializes the proxy locator object.
helpviewer_keywords: ["48eba170-eeed-4edf-b8d3-2f4541637129","FindFirstProxy","FindFirstProxy method [Media Foundation]","FindFirstProxy method [Media Foundation]","IMFNetProxyLocator interface","IMFNetProxyLocator interface [Media Foundation]","FindFirstProxy method","IMFNetProxyLocator.FindFirstProxy","IMFNetProxyLocator::FindFirstProxy","mf.imfnetproxylocator_findfirstproxy","mfidl/IMFNetProxyLocator::FindFirstProxy"]
old-location: mf\imfnetproxylocator_findfirstproxy.htm
tech.root: mf
ms.assetid: 48eba170-eeed-4edf-b8d3-2f4541637129
ms.date: 12/05/2018
ms.keywords: 48eba170-eeed-4edf-b8d3-2f4541637129, FindFirstProxy, FindFirstProxy method [Media Foundation], FindFirstProxy method [Media Foundation],IMFNetProxyLocator interface, IMFNetProxyLocator interface [Media Foundation],FindFirstProxy method, IMFNetProxyLocator.FindFirstProxy, IMFNetProxyLocator::FindFirstProxy, mf.imfnetproxylocator_findfirstproxy, mfidl/IMFNetProxyLocator::FindFirstProxy
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
 - IMFNetProxyLocator::FindFirstProxy
 - mfidl/IMFNetProxyLocator::FindFirstProxy
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
 - IMFNetProxyLocator.FindFirstProxy
---

# IMFNetProxyLocator::FindFirstProxy


## -description

Initializes the proxy locator object.

## -parameters

### -param pszHost [in]

Null-terminated wide-character string containing the hostname of the destination server.

### -param pszUrl [in]

Null-terminated wide-character string containing the destination URL.

### -param fReserved [in]

Reserved. Set to <b>FALSE</b>.

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