---
UID: NF:fsrm.IFsrmObject.Delete
title: IFsrmObject::Delete (fsrm.h)
description: Removes the object from the server's list of objects.
helpviewer_keywords: ["Delete","Delete method [File Server Resource Manager]","Delete method [File Server Resource Manager]","IFsrmObject interface","IFsrmObject interface [File Server Resource Manager]","Delete method","IFsrmObject.Delete","IFsrmObject::Delete","fs.ifsrmobject_delete","fsrm.ifsrmobject_delete","fsrm/IFsrmObject::Delete"]
old-location: fsrm\ifsrmobject_delete.htm
tech.root: fsrm
ms.assetid: ce8a17fe-377b-4a0e-9a95-7dc25a1411ce
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [File Server Resource Manager], Delete method [File Server Resource Manager],IFsrmObject interface, IFsrmObject interface [File Server Resource Manager],Delete method, IFsrmObject.Delete, IFsrmObject::Delete, fs.ifsrmobject_delete, fsrm.ifsrmobject_delete, fsrm/IFsrmObject::Delete
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
 - IFsrmObject::Delete
 - fsrm/IFsrmObject::Delete
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
 - IFsrmObject.Delete
---

# IFsrmObject::Delete


## -description

Removes the object from the server's list of objects.



## -returns

The method returns the following return values.

## -remarks

You must call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmObject::Commit</a> method to complete the delete operation.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>
