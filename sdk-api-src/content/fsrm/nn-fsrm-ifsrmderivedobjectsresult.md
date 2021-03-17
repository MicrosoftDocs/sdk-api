---
UID: NN:fsrm.IFsrmDerivedObjectsResult
title: IFsrmDerivedObjectsResult (fsrm.h)
description: Used to access the results when the source template calls the CommitAndUpdateDerived method.
helpviewer_keywords: ["IFsrmDerivedObjectsResult","IFsrmDerivedObjectsResult interface [File Server Resource Manager]","IFsrmDerivedObjectsResult interface [File Server Resource Manager]","described","fs.ifsrmderivedobjectsresult","fsrm.ifsrmderivedobjectsresult","fsrm/IFsrmDerivedObjectsResult"]
old-location: fsrm\ifsrmderivedobjectsresult.htm
tech.root: fsrm
ms.assetid: 1486d53a-d09a-4eff-ba07-b9dbb32e18ba
ms.date: 12/05/2018
ms.keywords: IFsrmDerivedObjectsResult, IFsrmDerivedObjectsResult interface [File Server Resource Manager], IFsrmDerivedObjectsResult interface [File Server Resource Manager],described, fs.ifsrmderivedobjectsresult, fsrm.ifsrmderivedobjectsresult, fsrm/IFsrmDerivedObjectsResult
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmDerivedObjectsResult
 - fsrm/IFsrmDerivedObjectsResult
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
 - IFsrmDerivedObjectsResult
---

# IFsrmDerivedObjectsResult interface


## -description

Used to access the results when the source template calls the <b>CommitAndUpdateDerived</b> method.

The following methods returns this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-commitandupdatederived">IFsrmFileScreenTemplate::CommitAndUpdateDerived</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplate-commitandupdatederived">IFsrmQuotaTemplate::CommitAndUpdateDerived</a>
</li>
</ul>