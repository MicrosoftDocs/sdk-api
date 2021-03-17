---
UID: NF:drt.DrtCreateNullSecurityProvider
title: DrtCreateNullSecurityProvider function (drt.h)
description: DrtCreateNullSecurityProvider function creates a null security provider. This security provider does not require nodes to authenticate keys.
helpviewer_keywords: ["DrtCreateNullSecurityProvider","DrtCreateNullSecurityProvider function [Distributed Routing Tables]","drt/DrtCreateNullSecurityProvider","p2p.drtcreatenullsecurityprovider"]
old-location: p2p\drtcreatenullsecurityprovider.htm
tech.root: p2p
ms.assetid: ba6e766f-784b-4609-8ad5-c1bfb0575f34
ms.date: 12/05/2018
ms.keywords: DrtCreateNullSecurityProvider, DrtCreateNullSecurityProvider function [Distributed Routing Tables], drt/DrtCreateNullSecurityProvider, p2p.drtcreatenullsecurityprovider
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtCreateNullSecurityProvider
 - drt/DrtCreateNullSecurityProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtCreateNullSecurityProvider
---

# DrtCreateNullSecurityProvider function


## -description

The <b>DrtCreateNullSecurityProvider</b> function creates a null security provider. This security provider does not require nodes to authenticate keys.

## -parameters

### -param ppSecurityProvider [out]

Pointer to the [DRT_SETTINGS](./ns-drt-drt_settings.md) structure.

## -returns

This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system cannot allocate memory for the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppDrtSecurityProvider</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_security_provider">DRT_SECURITY_PROVIDER</a>



<a href="/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider">DrtDeleteNullSecurityProvider</a>