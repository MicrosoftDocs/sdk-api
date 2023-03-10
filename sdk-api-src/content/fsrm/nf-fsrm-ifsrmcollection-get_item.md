---
UID: NF:fsrm.IFsrmCollection.get_Item
title: IFsrmCollection::get_Item (fsrm.h)
description: Retrieves the requested item from the collection. (IFsrmCollection.get_Item)
helpviewer_keywords: ["IFsrmCollection interface [File Server Resource Manager]","Item property","IFsrmCollection.Item","IFsrmCollection.get_Item","IFsrmCollection::Item","IFsrmCollection::get_Item","Item property [File Server Resource Manager]","Item property [File Server Resource Manager]","IFsrmCollection interface","fs.ifsrmcollection_item","fsrm.ifsrmcollection_item","fsrm/IFsrmCollection::Item","fsrm/IFsrmCollection::get_Item","get_Item"]
old-location: fsrm\ifsrmcollection_item.htm
tech.root: fsrm
ms.assetid: 95d35117-b9fb-46ae-b392-aa0c12717359
ms.date: 12/05/2018
ms.keywords: IFsrmCollection interface [File Server Resource Manager],Item property, IFsrmCollection.Item, IFsrmCollection.get_Item, IFsrmCollection::Item, IFsrmCollection::get_Item, Item property [File Server Resource Manager], Item property [File Server Resource Manager],IFsrmCollection interface, fs.ifsrmcollection_item, fsrm.ifsrmcollection_item, fsrm/IFsrmCollection::Item, fsrm/IFsrmCollection::get_Item, get_Item
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmCollection::get_Item
 - fsrm/IFsrmCollection::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmCollection.Item
 - IFsrmCollection.get_Item
---

# IFsrmCollection::get_Item


## -description

Retrieves the requested item from the collection.

This property is read-only.

## -parameters

## -remarks

If the item is an interface, the variant type is <b>VT_DISPATCH</b>. Call the 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the 
    <b>pdispVal</b> member of the variant to get an interface to the specific object.

If the item is an <b>HRESULT</b> value, the variant type is 
    <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to get the 
    <b>HRESULT</b> value.


#### Examples

For examples, see 
     <a href="/previous-versions/windows/desktop/fsrm/updating-a-file-screen">Updating a File Screen</a> and 
     <a href="/previous-versions/windows/desktop/fsrm/classifying-files">Classifying Files</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>
