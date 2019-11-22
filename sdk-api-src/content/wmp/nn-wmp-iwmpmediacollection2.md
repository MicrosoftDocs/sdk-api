---
UID: NN:wmp.IWMPMediaCollection2
title: IWMPMediaCollection2 (wmp.h)

description: The IWMPMediaCollection2 interface provides methods that supplement the IWMPMediaCollection interface.
old-location: wmp\iwmpmediacollection2.htm
tech.root: WMP
ms.assetid: 576e231e-542a-495c-ad1b-a246339c3cb1

ms.date: 12/05/2018
ms.keywords: IWMPMediaCollection2, IWMPMediaCollection2 interface [Windows Media Player], IWMPMediaCollection2 interface [Windows Media Player],described, IWMPMediaCollection2Interface, wmp.iwmpmediacollection2, wmp/IWMPMediaCollection2
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPMediaCollection2"
dev_langs:
 - c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPMediaCollection2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMediaCollection2 interface


## -description



The <b>IWMPMediaCollection2</b> interface provides methods that supplement the <b>IWMPMediaCollection</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMediaCollection2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection</a>. <b>IWMPMediaCollection2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPMediaCollection2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-createquery">createQuery</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPQuery</b> interface that represents a new query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getbyattributeandmediatype">getByAttributeAndMediaType</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that contains media items that have a specified attribute and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getplaylistbyquery">getPlaylistByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that contains media items that match the query conditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery">getStringCollectionByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPStringCollection</b> interface that contains the set of all string values for a specified attribute that match the query conditions.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

