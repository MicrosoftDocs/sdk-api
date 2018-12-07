---
UID: NN:bits3_0.IBitsPeerCacheAdministration
title: IBitsPeerCacheAdministration
author: windows-sdk-content
description: Use IBitsPeerCacheAdministration to manage the pool of peers from which you can download content.
old-location: bits\ibitspeercacheadministration.htm
tech.root: bits
ms.assetid: 5fa30b4e-f13c-4341-af65-a2e3d2703b96
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBitsPeerCacheAdministration, IBitsPeerCacheAdministration interface [BITS], IBitsPeerCacheAdministration interface [BITS],described, bits.ibitspeercacheadministration, bits3_0/IBitsPeerCacheAdministration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IBitsPeerCacheAdministration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheAdministration interface


## -description


Use <b>IBitsPeerCacheAdministration</b> to manage the pool of peers from which you can download content. 

To get this interface, call the <a href="https://msdn.microsoft.com/en-us/library/Aa363050(v=VS.85).aspx">IBackgroundCopyManager::QueryInterface</a> method, using __uuidof(IBitsPeerCacheAdministration) as the interface identifier. 
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitsPeerCacheAdministration</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBitsPeerCacheAdministration</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBitsPeerCacheAdministration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964273(v=VS.85).aspx">ClearPeers</a>
</td>
<td align="left" width="63%">
Removes all peers from the list of peers that can serve content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964274(v=VS.85).aspx">ClearRecords</a>
</td>
<td align="left" width="63%">
Removes all the records and files from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964275(v=VS.85).aspx">DeleteRecord</a>
</td>
<td align="left" width="63%">
Deletes a record and file from the cache based on the record identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964276(v=VS.85).aspx">DeleteUrl</a>
</td>
<td align="left" width="63%">
Deletes all cache records and the file from the cache for the given URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964277(v=VS.85).aspx">DiscoverPeers</a>
</td>
<td align="left" width="63%">
Generates a list of peers that can serve content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964278(v=VS.85).aspx">EnumPeers</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa964308(v=VS.85).aspx">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964279(v=VS.85).aspx">EnumRecords</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa964302(v=VS.85).aspx">IEnumBitsPeerCacheRecords</a> interface pointer that you use to enumerate the records in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964280(v=VS.85).aspx">GetConfigurationFlags</a>
</td>
<td align="left" width="63%">
Gets the configuration flags that determine whether the computer serves content to peers and can download content from peers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964282(v=VS.85).aspx">GetMaximumCacheSize</a>
</td>
<td align="left" width="63%">
Gets the maximum size of the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964286(v=VS.85).aspx">GetMaximumContentAge</a>
</td>
<td align="left" width="63%">
Gets the age by when files are removed from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964287(v=VS.85).aspx">GetRecord</a>
</td>
<td align="left" width="63%">
Gets a record from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964288(v=VS.85).aspx">SetConfigurationFlags</a>
</td>
<td align="left" width="63%">
Sets the configuration flags that determine whether the computer serves content to peers and can download content from peers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964289(v=VS.85).aspx">SetMaximumCacheSize</a>
</td>
<td align="left" width="63%">
Specifies the maximum size of the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964290(v=VS.85).aspx">SetMaximumContentAge</a>
</td>
<td align="left" width="63%">
Specifies when files are removed from the cache based on age.

</td>
</tr>
</table> 


## -remarks



 You should never have to manage the peer cache; BITS manages the cache for you.

You must have administrator privileges to modify the cache.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964240(v=VS.85).aspx">Administering the Peer Cache</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964314(v=VS.85).aspx">Peer Caching</a>
 

 

