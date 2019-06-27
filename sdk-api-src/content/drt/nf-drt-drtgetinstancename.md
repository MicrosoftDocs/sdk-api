---
UID: NF:drt.DrtGetInstanceName
title: DrtGetInstanceName function (drt.h)
author: windows-sdk-content
description: DrtGetInstanceName function retrieves the full name of the Distributed Routing Table instance that corresponds to the specified DRT handle.
old-location: p2p\drtgetinstancename.htm
tech.root: P2PSdk
ms.assetid: f69b745c-d990-42cf-8994-9640bcb7d1bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrtGetInstanceName, DrtGetInstanceName function [Distributed Routing Tables], drt/DrtGetInstanceName, p2p.drtgetinstancename
ms.topic: function
f1_keywords: 
 - "drt/DrtGetInstanceName"
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
req.lib: Drt.lib
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
 - DrtGetInstanceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrtGetInstanceName function


## -description


The <b>DrtGetInstanceName</b> function retrieves the full name of the Distributed Routing Table instance that corresponds to the specified DRT handle.


## -parameters




### -param hDrt [in]

Handle to the DRT instance.


### -param ulcbInstanceNameSize [in, out]

The length of the <i>pwzDrtInstanceName</i> buffer.


### -param pwzDrtInstanceName [out]

Contains the complete name of the DRT instance associated with <i>hDRT</i>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwzDrtInstanceName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hDrt</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwzDrtInstanceName</i> buffer is insufficient in size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>
 

 

