---
UID: NF:mfidl.IMFNetProxyLocator.Clone
title: IMFNetProxyLocator::Clone (mfidl.h)
description: Creates a new instance of the default proxy locator.
helpviewer_keywords: ["551372b3-b9aa-4057-8c14-19e582053e00","Clone","Clone method [Media Foundation]","Clone method [Media Foundation]","IMFNetProxyLocator interface","IMFNetProxyLocator interface [Media Foundation]","Clone method","IMFNetProxyLocator.Clone","IMFNetProxyLocator::Clone","mf.imfnetproxylocator_clone","mfidl/IMFNetProxyLocator::Clone"]
old-location: mf\imfnetproxylocator_clone.htm
tech.root: mf
ms.assetid: 551372b3-b9aa-4057-8c14-19e582053e00
ms.date: 12/05/2018
ms.keywords: 551372b3-b9aa-4057-8c14-19e582053e00, Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFNetProxyLocator interface, IMFNetProxyLocator interface [Media Foundation],Clone method, IMFNetProxyLocator.Clone, IMFNetProxyLocator::Clone, mf.imfnetproxylocator_clone, mfidl/IMFNetProxyLocator::Clone
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
 - IMFNetProxyLocator::Clone
 - mfidl/IMFNetProxyLocator::Clone
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
 - IMFNetProxyLocator.Clone
---

# IMFNetProxyLocator::Clone


## -description

Creates a new instance of the default proxy locator.

## -parameters

### -param ppProxyLocator [out]

Receives a pointer to the new proxy locator object's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator">IMFNetProxyLocator</a> interface. The caller must release the interface.

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