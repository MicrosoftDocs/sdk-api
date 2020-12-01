---
UID: NF:fsrm.IFsrmCollection.GetById
title: IFsrmCollection::GetById (fsrm.h)
description: Retrieves the specified object from the collection.
helpviewer_keywords: ["GetById","GetById method [File Server Resource Manager]","GetById method [File Server Resource Manager]","IFsrmCollection interface","IFsrmCollection interface [File Server Resource Manager]","GetById method","IFsrmCollection.GetById","IFsrmCollection::GetById","fs.ifsrmcollection_getbyid","fsrm.ifsrmcollection_getbyid","fsrm/IFsrmCollection::GetById"]
old-location: fsrm\ifsrmcollection_getbyid.htm
tech.root: fsrm
ms.assetid: 6d6be809-bfe6-46ad-9156-288da834ff13
ms.date: 12/05/2018
ms.keywords: GetById, GetById method [File Server Resource Manager], GetById method [File Server Resource Manager],IFsrmCollection interface, IFsrmCollection interface [File Server Resource Manager],GetById method, IFsrmCollection.GetById, IFsrmCollection::GetById, fs.ifsrmcollection_getbyid, fsrm.ifsrmcollection_getbyid, fsrm/IFsrmCollection::GetById
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
 - IFsrmCollection::GetById
 - fsrm/IFsrmCollection::GetById
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
 - IFsrmCollection.GetById
---

# IFsrmCollection::GetById


## -description

Retrieves the specified object from the collection.

## -parameters

### -param id [in]

Identifies the object to retrieve from the collection.

### -param entry [out]

A <b>VARIANT</b> that contains the retrieved object. The variant type is <b>VT_DISPATCH</b>. Use the <b>pdispVal</b> member to access the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface of the object.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>