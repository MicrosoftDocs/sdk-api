---
UID: NF:bits3_0.IBitsPeer.IsAvailable
title: IBitsPeer::IsAvailable
author: windows-sdk-content
description: Determines whether the peer is available (online) to serve content.
old-location: bits\ibitspeer_isavailable.htm
tech.root: Bits
ms.assetid: e38166da-2139-4108-bb8a-74bb7a7997c1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBitsPeer interface [BITS],IsAvailable method, IBitsPeer.IsAvailable, IBitsPeer::IsAvailable, IsAvailable, IsAvailable method [BITS], IsAvailable method [BITS],IBitsPeer interface, bits.ibitspeer_isavailable, bits3_0/IBitsPeer::IsAvailable
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
 - IBitsPeer.IsAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeer::IsAvailable


## -description


Determines whether the peer is available (online) to serve content.


## -parameters




### -param pOnline [out]

<b>TRUE</b> if the peer is available to serve content, otherwise, <b>FALSE</b>.


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



If this peer goes offline while BITS is downloading content from it, BITS immediately begins downloading from the origin server. 

If the peer stays offline for an extended period of time, BITS removes the peer from the neighborhood.




## -see-also




<a href="https://msdn.microsoft.com/617b88d4-6c3e-4c33-9bfa-6d9f6f629866">IBitsPeer</a>
 

 

