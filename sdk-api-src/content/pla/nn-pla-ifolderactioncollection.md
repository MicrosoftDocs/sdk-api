---
UID: NN:pla.IFolderActionCollection
title: IFolderActionCollection (pla.h)
description: Manages a collection of FolderAction objects.To get this interface, access the IDataManager::FolderActions property.
helpviewer_keywords: ["IFolderActionCollection","IFolderActionCollection interface [PLA]","IFolderActionCollection interface [PLA]","described","base.ifolderactioncollection","pla.ifolderactioncollection","pla/IFolderActionCollection"]
old-location: pla\ifolderactioncollection.htm
tech.root: PLA
ms.assetid: 9b0ab26f-7e91-4d7a-9fd7-73332601dd7b
ms.date: 12/05/2018
ms.keywords: IFolderActionCollection, IFolderActionCollection interface [PLA], IFolderActionCollection interface [PLA],described, base.ifolderactioncollection, pla.ifolderactioncollection, pla/IFolderActionCollection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderActionCollection
 - pla/IFolderActionCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IFolderActionCollection
---

# IFolderActionCollection interface


## -description

Manages a collection of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ifolderaction">FolderAction</a> objects.

To get this interface, access the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_folderactions">IDataManager::FolderActions</a> property.

## -inheritance

The <b>IFolderActionCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFolderActionCollection</b> also has these types of members:

## -remarks

You can add one or more <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ifolderaction">IFolderAction</a> instances. Each instance determines when a folder action occurs. For example, one instance  can trigger folder actions to occur at week one (<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ifolderaction-get_age">IFolderAction::Age</a> is 7) and a second instance can trigger folder actions to occur at week 10 (<b>Age</b> is 10).
