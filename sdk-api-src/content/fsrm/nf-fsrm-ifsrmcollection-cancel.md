---
UID: NF:fsrm.IFsrmCollection.Cancel
title: IFsrmCollection::Cancel (fsrm.h)
description: Cancels the collection of objects when the objects are collected asynchronously.
helpviewer_keywords: ["Cancel","Cancel method [File Server Resource Manager]","Cancel method [File Server Resource Manager]","IFsrmCollection interface","IFsrmCollection interface [File Server Resource Manager]","Cancel method","IFsrmCollection.Cancel","IFsrmCollection::Cancel","fs.ifsrmcollection_cancel","fsrm.ifsrmcollection_cancel","fsrm/IFsrmCollection::Cancel"]
old-location: fsrm\ifsrmcollection_cancel.htm
tech.root: fsrm
ms.assetid: f51f1a8d-a857-4a17-96ca-1f3ed391b7d7
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [File Server Resource Manager], Cancel method [File Server Resource Manager],IFsrmCollection interface, IFsrmCollection interface [File Server Resource Manager],Cancel method, IFsrmCollection.Cancel, IFsrmCollection::Cancel, fs.ifsrmcollection_cancel, fsrm.ifsrmcollection_cancel, fsrm/IFsrmCollection::Cancel
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
 - IFsrmCollection::Cancel
 - fsrm/IFsrmCollection::Cancel
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
 - IFsrmCollection.Cancel
---

# IFsrmCollection::Cancel


## -description

Cancels the collection of objects when the objects are collected asynchronously.<div class="alert"><b>Note</b>  Asynchronous collections are not supported by FSRM, therefore this method is not implemented in the FSRM library.</div>
<div> </div>



## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>
