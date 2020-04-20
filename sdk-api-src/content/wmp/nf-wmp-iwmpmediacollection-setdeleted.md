---
UID: NF:wmp.IWMPMediaCollection.setDeleted
title: IWMPMediaCollection::setDeleted (wmp.h)
description: The setDeleted method moves the specified media item to the deleted items folder.helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","setDeleted method","IWMPMediaCollection.setDeleted","IWMPMediaCollection::setDeleted","IWMPMediaCollectionsetDeleted","setDeleted","setDeleted method [Windows Media Player]","setDeleted method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_setdeleted","wmp/IWMPMediaCollection::setDeleted"]
old-location: wmp\iwmpmediacollection_setdeleted.htm
tech.root: WMP
ms.assetid: 4bba1e7a-3c1f-4f69-b4ab-68a9cf3b97d0
ms.date: 12/05/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],setDeleted method, IWMPMediaCollection.setDeleted, IWMPMediaCollection::setDeleted, IWMPMediaCollectionsetDeleted, setDeleted, setDeleted method [Windows Media Player], setDeleted method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_setdeleted, wmp/IWMPMediaCollection::setDeleted
f1_keywords:
- wmp/IWMPMediaCollection.setDeleted
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPMediaCollection.setDeleted
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMediaCollection::setDeleted


## -description



The <b>setDeleted</b> method moves the specified media item to the deleted items folder.




## -parameters




### -param pItem [in]

Pointer to an <b>IWMPMedia</b> interface for the item to be moved.


### -param varfIsDeleted [in]

Specifies whether the item should be moved. This value must always be true.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method does not remove files from the user's computer.

Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>
 

 

