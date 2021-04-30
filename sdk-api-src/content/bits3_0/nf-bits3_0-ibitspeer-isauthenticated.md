---
UID: NF:bits3_0.IBitsPeer.IsAuthenticated
title: IBitsPeer::IsAuthenticated (bits3_0.h)
description: Determines whether the peer is authenticated.
helpviewer_keywords: ["IBitsPeer interface [BITS]","IsAuthenticated method","IBitsPeer.IsAuthenticated","IBitsPeer::IsAuthenticated","IsAuthenticated","IsAuthenticated method [BITS]","IsAuthenticated method [BITS]","IBitsPeer interface","bits.ibitspeer_isauthenticated","bits3_0/IBitsPeer::IsAuthenticated"]
old-location: bits\ibitspeer_isauthenticated.htm
tech.root: Bits
ms.assetid: 64718331-32a9-40ba-90f2-9dd9d8fea3e4
ms.date: 12/05/2018
ms.keywords: IBitsPeer interface [BITS],IsAuthenticated method, IBitsPeer.IsAuthenticated, IBitsPeer::IsAuthenticated, IsAuthenticated, IsAuthenticated method [BITS], IsAuthenticated method [BITS],IBitsPeer interface, bits.ibitspeer_isauthenticated, bits3_0/IBitsPeer::IsAuthenticated
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBitsPeer::IsAuthenticated
 - bits3_0/IBitsPeer::IsAuthenticated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeer.IsAuthenticated
---

# IBitsPeer::IsAuthenticated


## -description

Determines whether the peer is authenticated.

## -parameters

### -param pAuth [out]

<b>TRUE</b> if the peer is authenticated, otherwise, <b>FALSE</b>.

## -returns

The method returns the following return values.

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
Success

</td>
</tr>
</table>

## -remarks

BITS cannot download content from an unauthenticated peer. When peers are detected, they are initially not authenticated.  BITS contacts peers when downloading a job that is enabled for peercaching; BITS authenticates a given peer the first time it is contacted.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeer">IBitsPeer</a>