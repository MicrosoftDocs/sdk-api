---
UID: NN:mswmdm.IWMDMStorage2
title: IWMDMStorage2 (mswmdm.h)
description: The IWMDMStorage2 interface extends IWMDMStorage by making it possible to get a child storage by name, and to get and set extended attributes. IWMDMStorage3 interface extends this interface by supporting metadata.
old-location: wmdm\iwmdmstorage2.htm
tech.root: WMDM
ms.assetid: 1283a5b5-d893-4795-a50a-5a3bd6fce8d5
ms.date: 12/05/2018
ms.keywords: IWMDMStorage2, IWMDMStorage2 interface [windows Media Device Manager], IWMDMStorage2 interface [windows Media Device Manager],described, IWMDMStorage2Interface, mswmdm/IWMDMStorage2, wmdm.iwmdmstorage2
ms.topic: interface
f1_keywords:
- mswmdm/IWMDMStorage2
dev_langs:
- c++
req.header: mswmdm.h
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
- mswmdm.h
api_name:
- IWMDMStorage2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorage2 interface


## -description



The <b>IWMDMStorage2</b> interface extends <b>IWMDMStorage</b> by making it possible to get a child storage by name, and to get and set extended attributes. <b>IWMDMStorage3</b> interface extends this interface by supporting metadata.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage</a>. <b>IWMDMStorage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2">GetAttributes2</a>
</td>
<td align="left" width="63%">
Retrieves extended attributes of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getstorage">GetStorage</a>
</td>
<td align="left" width="63%">
Retrieves a child storage by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2">SetAttributes2</a>
</td>
<td align="left" width="63%">
Sets extended attributes of the storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4">IWMDMStorage4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

