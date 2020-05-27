---
UID: NN:mswmdm.IWMDMStorageControl3
title: IWMDMStorageControl3 (mswmdm.h)
description: The IWMDMStorageControl3 interface extends IWMDMStorageControl2 by providing an Insert method that accepts an IWMDMMetaData interface pointer.
helpviewer_keywords: ["IWMDMStorageControl3","IWMDMStorageControl3 interface [windows Media Device Manager]","IWMDMStorageControl3 interface [windows Media Device Manager]","described","IWMDMStorageControl3Interface","mswmdm/IWMDMStorageControl3","wmdm.iwmdmstoragecontrol3"]
old-location: wmdm\iwmdmstoragecontrol3.htm
tech.root: WMDM
ms.assetid: bc5165c2-791d-4549-a271-78728625b219
ms.date: 12/05/2018
ms.keywords: IWMDMStorageControl3, IWMDMStorageControl3 interface [windows Media Device Manager], IWMDMStorageControl3 interface [windows Media Device Manager],described, IWMDMStorageControl3Interface, mswmdm/IWMDMStorageControl3, wmdm.iwmdmstoragecontrol3
f1_keywords:
- mswmdm/IWMDMStorageControl3
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
- IWMDMStorageControl3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorageControl3 interface


## -description



The <b>IWMDMStorageControl3</b> interface extends <b>IWMDMStorageControl2</b> by providing an <b>Insert</b> method that accepts an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData</a> interface pointer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorageControl3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2">IWMDMStorageControl2</a>. <b>IWMDMStorageControl3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorageControl3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3">Insert3</a>
</td>
<td align="left" width="63%">
Puts content into/next to the storage. Extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2">IWMDMStorageControl2::Insert2</a> method by allowing the application to pass in an <b>IWMDMMetaData</b> interface pointer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2">IWMDMStorageControl2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

