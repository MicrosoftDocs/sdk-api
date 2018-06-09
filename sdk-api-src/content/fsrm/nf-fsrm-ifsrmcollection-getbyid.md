---
UID: NF:fsrm.IFsrmCollection.GetById
title: IFsrmCollection::GetById
author: windows-sdk-content
description: Retrieves the specified object from the collection.
old-location: fsrm\ifsrmcollection_getbyid.htm
old-project: Fsrm
ms.assetid: 6d6be809-bfe6-46ad-9156-288da834ff13
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetById, GetById method [File Server Resource Manager], GetById method [File Server Resource Manager],IFsrmCollection interface, IFsrmCollection interface [File Server Resource Manager],GetById method, IFsrmCollection.GetById, IFsrmCollection::GetById, fs.ifsrmcollection_getbyid, fsrm.ifsrmcollection_getbyid, fsrm/IFsrmCollection::GetById
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmCollection.GetById
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmCollection::GetById


## -description


Retrieves the specified object from the collection.


## -parameters




### -param id [in]

Identifies the object to retrieve from the collection.


### -param entry [out]

A <b>VARIANT</b> that contains the retrieved object. The variant type is <b>VT_DISPATCH</b>. Use the <b>pdispVal</b> member to access the <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface of the object.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

