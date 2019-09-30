---
UID: NN:wmp.IWMPStringCollection
title: IWMPStringCollection (wmp.h)
author: windows-sdk-content
description: The IWMPStringCollection interface provides methods that work with a collection of strings.
old-location: wmp\iwmpstringcollection.htm
tech.root: WMP
ms.assetid: 8cdabea9-7e37-4e63-9d6c-b6f63aa536ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPStringCollection, IWMPStringCollection interface [Windows Media Player], IWMPStringCollection interface [Windows Media Player],described, IWMPStringCollectionInterface, wmp.iwmpstringcollection, wmp/IWMPStringCollection
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPStringCollection"
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
 - IWMPStringCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPStringCollection interface


## -description



The <b>IWMPStringCollection</b> interface provides methods that work with a collection of strings.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPStringCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPStringCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPStringCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpstringcollection-get_count">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the string collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpstringcollection-item">item</a>
</td>
<td align="left" width="63%">
Retrieves the string at the specified index.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPStringCollection</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection</a>
</td>
<td>
<a href="https://msdn.microsoft.com/c3699acb-58a1-4efa-a42c-c84534abca96">getAttributeStringCollection</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

