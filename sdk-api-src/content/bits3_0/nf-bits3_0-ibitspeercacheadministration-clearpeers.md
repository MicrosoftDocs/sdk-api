---
UID: NF:bits3_0.IBitsPeerCacheAdministration.ClearPeers
title: IBitsPeerCacheAdministration::ClearPeers
author: windows-sdk-content
description: Removes all peers from the list of peers that can serve content.
old-location: bits\ibitspeercacheadministration_clearpeers.htm
old-project: bits
ms.assetid: 79a739ed-7618-410a-a6df-fab11794d932
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ClearPeers, ClearPeers method [BITS], ClearPeers method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],ClearPeers method, IBitsPeerCacheAdministration.ClearPeers, IBitsPeerCacheAdministration::ClearPeers, bits.ibitspeercacheadministration_clearpeers, bits3_0/IBitsPeerCacheAdministration::ClearPeers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.redist: 
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
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheAdministration.ClearPeers
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheAdministration::ClearPeers


## -description


Removes all peers from the list of peers that can serve content.


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

BITS automatically discovers new peers when a job requests content from a peer. You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa964277(v=VS.85).aspx">IBitsPeerCacheAdministration::DiscoverPeers</a> method to force discovery of peers.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964272(v=VS.85).aspx">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964277(v=VS.85).aspx">IBitsPeerCacheAdministration::DiscoverPeers</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964278(v=VS.85).aspx">IBitsPeerCacheAdministration::EnumPeers</a>
 

 

