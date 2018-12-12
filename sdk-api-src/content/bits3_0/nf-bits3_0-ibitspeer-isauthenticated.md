---
UID: NF:bits3_0.IBitsPeer.IsAuthenticated
title: IBitsPeer::IsAuthenticated
author: windows-sdk-content
description: Determines whether the peer is authenticated.
old-location: bits\ibitspeer_isauthenticated.htm
tech.root: bits
ms.assetid: 64718331-32a9-40ba-90f2-9dd9d8fea3e4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBitsPeer interface [BITS],IsAuthenticated method, IBitsPeer.IsAuthenticated, IBitsPeer::IsAuthenticated, IsAuthenticated, IsAuthenticated method [BITS], IsAuthenticated method [BITS],IBitsPeer interface, bits.ibitspeer_isauthenticated, bits3_0/IBitsPeer::IsAuthenticated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/617b88d4-6c3e-4c33-9bfa-6d9f6f629866">IBitsPeer</a>
 

 

