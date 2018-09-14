---
UID: NF:bits3_0.IBitsPeerCacheAdministration.DiscoverPeers
title: IBitsPeerCacheAdministration::DiscoverPeers
author: windows-sdk-content
description: Generates a list of peers that can serve content.
old-location: bits\ibitspeercacheadministration_discoverpeers.htm
tech.root: Bits
ms.assetid: c83632c2-5d01-48ab-93ef-961778c2379a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DiscoverPeers, DiscoverPeers method [BITS], DiscoverPeers method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],DiscoverPeers method, IBitsPeerCacheAdministration.DiscoverPeers, IBitsPeerCacheAdministration::DiscoverPeers, bits.ibitspeercacheadministration_discoverpeers, bits3_0/IBitsPeerCacheAdministration::DiscoverPeers
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
 - IBitsPeerCacheAdministration.DiscoverPeers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheAdministration::DiscoverPeers


## -description


Generates a list of peers that can serve content.


## -parameters






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



You should not have to call this method.

BITS automatically discovers new peers when a job requests content from a peer and there are not enough peers in the client's peer list. Peers must be in the same Windows domain and subnet as the client and be enabled to serve content to peers.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964272(v=VS.85).aspx">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964273(v=VS.85).aspx">IBitsPeerCacheAdministration::ClearPeers</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964278(v=VS.85).aspx">IBitsPeerCacheAdministration::EnumPeers</a>
 

 

