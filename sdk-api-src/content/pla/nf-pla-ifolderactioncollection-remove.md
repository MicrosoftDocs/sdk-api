---
UID: NF:pla.IFolderActionCollection.Remove
title: IFolderActionCollection::Remove (pla.h)
description: Removes a folder action from the collection based on the specified index.helpviewer_keywords: ["IFolderActionCollection interface [PLA]","Remove method","IFolderActionCollection.Remove","IFolderActionCollection::Remove","Remove","Remove method [PLA]","Remove method [PLA]","IFolderActionCollection interface","base.ifolderactioncollection_remove","pla.ifolderactioncollection_remove","pla/IFolderActionCollection::Remove"]
old-location: pla\ifolderactioncollection_remove.htm
tech.root: PLA
ms.assetid: b0894d3f-13d1-4f71-9171-592640d70969
ms.date: 12/05/2018
ms.keywords: IFolderActionCollection interface [PLA],Remove method, IFolderActionCollection.Remove, IFolderActionCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],IFolderActionCollection interface, base.ifolderactioncollection_remove, pla.ifolderactioncollection_remove, pla/IFolderActionCollection::Remove
f1_keywords:
- pla/IFolderActionCollection.Remove
dev_langs:
- c++
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Pla.dll
api_name:
- IFolderActionCollection.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderActionCollection::Remove


## -description


Removes a folder action from the collection based on the specified index.


## -parameters




### -param Index [in]

The zero-based index of the folder action to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ifolderaction">IFolderAction</a> interface to be removed.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ifolderactioncollection">IFolderActionCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-add">IFolderActionCollection::Add</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-clear">IFolderActionCollection::Clear</a>
 

 

