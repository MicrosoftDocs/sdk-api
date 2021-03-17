---
UID: NN:pla.IFolderAction
title: IFolderAction (pla.h)
description: Specifies the actions that the data manager is to take on each folder under the data collector set's root path if both conditions (age and size) are met. To get this interface, call the IFolderActionCollection::CreateFolderAction method.
helpviewer_keywords: ["IFolderAction","IFolderAction interface [PLA]","IFolderAction interface [PLA]","described","base.ifolderaction","pla.ifolderaction","pla/IFolderAction"]
old-location: pla\ifolderaction.htm
tech.root: PLA
ms.assetid: a3942d5f-9ec4-4461-84f9-f2fae3971e23
ms.date: 12/05/2018
ms.keywords: IFolderAction, IFolderAction interface [PLA], IFolderAction interface [PLA],described, base.ifolderaction, pla.ifolderaction, pla/IFolderAction
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
 - IFolderAction
 - pla/IFolderAction
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
 - IFolderAction
---

# IFolderAction interface


## -description

Specifies the actions that the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">data manager</a> is to take on each folder under the data collector set's <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">root path</a> if both conditions (age and size) are met. 

To get this interface, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-createfolderaction">IFolderActionCollection::CreateFolderAction</a> method.

## -remarks

To create the object from a script, use the Pla.FolderAction program identifier.

For an example that shows the XML that you can use to initialize this object if you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">IDataCollectorSet::SetXml</a> method, see the Remarks section of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>.  When you specify the XML to create the object, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the set, the XML includes all elements.