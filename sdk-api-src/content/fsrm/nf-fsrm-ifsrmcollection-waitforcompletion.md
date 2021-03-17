---
UID: NF:fsrm.IFsrmCollection.WaitForCompletion
title: IFsrmCollection::WaitForCompletion (fsrm.h)
description: Limits the time that an asynchronous collection can take to collect the objects.
helpviewer_keywords: ["IFsrmCollection interface [File Server Resource Manager]","WaitForCompletion method","IFsrmCollection.WaitForCompletion","IFsrmCollection::WaitForCompletion","WaitForCompletion","WaitForCompletion method [File Server Resource Manager]","WaitForCompletion method [File Server Resource Manager]","IFsrmCollection interface","fs.ifsrmcollection_waitforcompletion","fsrm.ifsrmcollection_waitforcompletion","fsrm/IFsrmCollection::WaitForCompletion"]
old-location: fsrm\ifsrmcollection_waitforcompletion.htm
tech.root: fsrm
ms.assetid: 83b9feb5-5f10-4c27-be3e-b267a0356aa2
ms.date: 12/05/2018
ms.keywords: IFsrmCollection interface [File Server Resource Manager],WaitForCompletion method, IFsrmCollection.WaitForCompletion, IFsrmCollection::WaitForCompletion, WaitForCompletion, WaitForCompletion method [File Server Resource Manager], WaitForCompletion method [File Server Resource Manager],IFsrmCollection interface, fs.ifsrmcollection_waitforcompletion, fsrm.ifsrmcollection_waitforcompletion, fsrm/IFsrmCollection::WaitForCompletion
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
 - IFsrmCollection::WaitForCompletion
 - fsrm/IFsrmCollection::WaitForCompletion
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
 - IFsrmCollection.WaitForCompletion
---

# IFsrmCollection::WaitForCompletion


## -description

Limits the time that an asynchronous collection can take to collect the objects.<div class="alert"><b>Note</b>  Asynchronous collections are not supported by FSRM, therefore this method always sets the <i>completed</i> parameter to <b>VARIANT_TRUE</b>.</div>
<div> </div>

## -parameters

### -param waitSeconds [in]

The number of seconds to wait for the collection to finish collecting objects. To wait indefinitely, set this parameter to –1.

### -param completed [out]

Is <b>VARIANT_TRUE</b> if the collection finished collecting objects in the time specified; otherwise, <b>VARIANT_FALSE</b>.

## -returns

This method is not supported and always returns <b>S_OK</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>