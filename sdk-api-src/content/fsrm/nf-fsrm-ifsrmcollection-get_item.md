---
UID: NF:fsrm.IFsrmCollection.get_Item
title: IFsrmCollection::get_Item
author: windows-sdk-content
description: Retrieves the requested item from the collection.
old-location: fsrm\ifsrmcollection_item.htm
tech.root: fsrm
ms.assetid: 95d35117-b9fb-46ae-b392-aa0c12717359
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmCollection interface [File Server Resource Manager],Item property, IFsrmCollection.Item, IFsrmCollection.get_Item, IFsrmCollection::Item, IFsrmCollection::get_Item, Item property [File Server Resource Manager], Item property [File Server Resource Manager],IFsrmCollection interface, fs.ifsrmcollection_item, fsrm.ifsrmcollection_item, fsrm/IFsrmCollection::Item, fsrm/IFsrmCollection::get_Item, get_Item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmCollection::get_Item


## -description


Retrieves the requested item from the collection.

This property is read-only.


## -parameters


## -remarks



If the item is an interface, the variant type is <b>VT_DISPATCH</b>. Call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on the 
    <b>pdispVal</b> member of the variant to get an interface to the specific object.

If the item is an <b>HRESULT</b> value, the variant type is 
    <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to get the 
    <b>HRESULT</b> value.


#### Examples

For examples, see 
     <a href="https://msdn.microsoft.com/298e7e37-709a-4b13-87d3-605d540d8f85">Updating a File Screen</a> and 
     <a href="https://msdn.microsoft.com/94e382d6-3e18-4c80-aed2-4c2d58699236">Classifying Files</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

