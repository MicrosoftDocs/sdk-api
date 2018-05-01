---
UID: NN:bits3_0.IBitsPeerCacheAdministration
title: IBitsPeerCacheAdministration
author: windows-driver-content
description: Use IBitsPeerCacheAdministration to manage the pool of peers from which you can download content.
old-location: bits\ibitspeercacheadministration.htm
old-project: Bits
ms.assetid: 5fa30b4e-f13c-4341-af65-a2e3d2703b96
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: IBitsPeerCacheAdministration, IBitsPeerCacheAdministration interface [BITS], IBitsPeerCacheAdministration interface [BITS], described, bits.ibitspeercacheadministration, bits3_0/IBitsPeerCacheAdministration
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
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits.lib
-	Bits.dll
api_name:
-	IBitsPeerCacheAdministration
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheAdministration interface


## -description


Use <b>IBitsPeerCacheAdministration</b> to manage the pool of peers from which you can download content. 

To get this interface, call the <a href="https://msdn.microsoft.com/fc98dfb3-7e10-421d-b722-223bd8a65330">IBackgroundCopyManager::QueryInterface</a> method, using __uuidof(IBitsPeerCacheAdministration) as the interface identifier. 
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitsPeerCacheAdministration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBitsPeerCacheAdministration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/79a739ed-7618-410a-a6df-fab11794d932">ClearPeers</a>
</td>
<td align="left" width="63%">
Removes all peers from the list of peers that can serve content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96e18c5d-6c76-4953-8e8e-3e98943478d8">ClearRecords</a>
</td>
<td align="left" width="63%">
Removes all the records and files from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c86199c3-9fe7-4d8f-8b33-b12b65b94e54">DeleteRecord</a>
</td>
<td align="left" width="63%">
Deletes a record and file from the cache based on the record identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4849830-62fa-4bf4-bfad-59bcdbf1a10e">DeleteUrl</a>
</td>
<td align="left" width="63%">
Deletes all cache records and the file from the cache for the given URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c83632c2-5d01-48ab-93ef-961778c2379a">DiscoverPeers</a>
</td>
<td align="left" width="63%">
Generates a list of peers that can serve content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8786d7d8-9ffb-4492-9834-90b97f97e4cf">EnumPeers</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/2715a58c-ba76-4223-ad9e-453d029e0eda">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b471cee0-0ad0-4488-9819-e524e50dbc76">EnumRecords</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/680c1468-d780-44a3-9048-c7c3928234f9">IEnumBitsPeerCacheRecords</a> interface pointer that you use to enumerate the records in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caa54ee0-c771-47e7-95d1-26a812f0f95f">GetConfigurationFlags</a>
</td>
<td align="left" width="63%">
Gets the configuration flags that determine whether the computer serves content to peers and can download content from peers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea0e6f7-c674-4088-9085-5f6246681009">GetMaximumCacheSize</a>
</td>
<td align="left" width="63%">
Gets the maximum size of the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b6b0c97-9906-464d-b267-5adde1919a45">GetMaximumContentAge</a>
</td>
<td align="left" width="63%">
Gets the age by when files are removed from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dd32e9c-bf4e-4dbf-aa9f-9ffbf98d3f1c">GetRecord</a>
</td>
<td align="left" width="63%">
Gets a record from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ede7c58-bc6d-4930-bca6-e4f26f97c648">SetConfigurationFlags</a>
</td>
<td align="left" width="63%">
Sets the configuration flags that determine whether the computer serves content to peers and can download content from peers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/064376cf-8865-45a1-a63a-1096bc0d58ce">SetMaximumCacheSize</a>
</td>
<td align="left" width="63%">
Specifies the maximum size of the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/815d9e48-f1f0-4c40-a277-d78db9d6ace1">SetMaximumContentAge</a>
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




<a href="https://msdn.microsoft.com/a33a43e5-02f9-4902-ad3a-ec65b0d80520">Administering the Peer Cache</a>



<a href="https://msdn.microsoft.com/4197eed3-1812-4440-99e7-9462635ef6ad">Peer Caching</a>
 

 

