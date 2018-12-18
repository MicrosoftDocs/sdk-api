---
UID: NF:drt.DrtCreateNullSecurityProvider
title: DrtCreateNullSecurityProvider function
author: windows-sdk-content
description: DrtCreateNullSecurityProvider function creates a null security provider. This security provider does not require nodes to authenticate keys.
old-location: p2p\drtcreatenullsecurityprovider.htm
tech.root: P2PSdk
ms.assetid: ba6e766f-784b-4609-8ad5-c1bfb0575f34
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrtCreateNullSecurityProvider, DrtCreateNullSecurityProvider function [Distributed Routing Tables], drt/DrtCreateNullSecurityProvider, p2p.drtcreatenullsecurityprovider
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtCreateNullSecurityProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrtCreateNullSecurityProvider function


## -description


The <b>DrtCreateNullSecurityProvider</b> function creates a null security provider. This security provider does not require nodes to authenticate keys.


## -parameters




### -param ppSecurityProvider [out]

Pointer to the <a href="https://msdn.microsoft.com/1eedfff3-d561-462e-bad0-45e7bc46fb1a">DRT_SECURITY_PROVIDER</a> module to be included in the <a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a> structure.


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




<a href="https://msdn.microsoft.com/1eedfff3-d561-462e-bad0-45e7bc46fb1a">DRT_SECURITY_PROVIDER</a>



<a href="https://msdn.microsoft.com/950a43f3-1c1d-4fb3-988b-d58ac9eff2f8">DrtDeleteNullSecurityProvider</a>
 

 

