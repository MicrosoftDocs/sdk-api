---
UID: NF:drt.DrtGetInstanceNameSize
title: DrtGetInstanceNameSize function (drt.h)
description: The DrtGetInstanceNameSize function returns the size of the Distributed Routing Table instance name.
helpviewer_keywords: ["DrtGetInstanceNameSize","DrtGetInstanceNameSize function [Peer Networking]","drt/DrtGetInstanceNameSize","p2p.drtgetinstancenamesize"]
old-location: p2p\drtgetinstancenamesize.htm
tech.root: p2p
ms.assetid: b600ee27-bcea-4496-888f-1300f74d41e4
ms.date: 12/05/2018
ms.keywords: DrtGetInstanceNameSize, DrtGetInstanceNameSize function [Peer Networking], drt/DrtGetInstanceNameSize, p2p.drtgetinstancenamesize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtGetInstanceNameSize
 - drt/DrtGetInstanceNameSize
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
 - DrtGetInstanceNameSize
---

# DrtGetInstanceNameSize function


## -description

The <b>DrtGetInstanceNameSize</b> function returns the size of the Distributed Routing Table instance name.

## -parameters

### -param hDrt [in]

Handle to the target DRT instance.

### -param pulcbInstanceNameSize [out]

The length of the DRT instance name.

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
<i>pulcbInstanceNameSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hDrt</i> handle is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>