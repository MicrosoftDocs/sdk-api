---
UID: NN:wmp.IWMPCdromCollection
title: IWMPCdromCollection (wmp.h)
description: The IWMPCdromCollection interface provides a way to organize and access a collection of CD or DVD drives.
old-location: wmp\iwmpcdromcollection.htm
tech.root: WMP
ms.assetid: ba55ac32-149d-4f7b-a2bb-1fdb0be806cd
ms.date: 12/05/2018
ms.keywords: IWMPCdromCollection, IWMPCdromCollection interface [Windows Media Player], IWMPCdromCollection interface [Windows Media Player],described, IWMPCdromCollectionInterface, wmp.iwmpcdromcollection, wmp/IWMPCdromCollection
f1_keywords:
- wmp/IWMPCdromCollection
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
- IWMPCdromCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCdromCollection interface


## -description



The <b>IWMPCdromCollection</b> interface provides a way to organize and access a collection of CD or DVD drives.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCdromCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPCdromCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPCdromCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the number of available CD and DVD drives on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-getbydrivespecifier">getByDriveSpecifier</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPCdrom</b> interface associated with a particular drive letter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item">item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPCdrom</b> interface at the given index.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPCdromCollection</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection">get_cdromCollection</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcdrom">IWMPCdrom Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

