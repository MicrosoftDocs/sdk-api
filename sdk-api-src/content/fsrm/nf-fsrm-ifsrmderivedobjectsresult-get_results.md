---
UID: NF:fsrm.IFsrmDerivedObjectsResult.get_Results
title: IFsrmDerivedObjectsResult::get_Results (fsrm.h)
description: Retrieves the HRESULT values that indicate the success or failure of the update for each derived object.
helpviewer_keywords: ["IFsrmDerivedObjectsResult interface [File Server Resource Manager]","Results property","IFsrmDerivedObjectsResult.Results","IFsrmDerivedObjectsResult.get_Results","IFsrmDerivedObjectsResult::Results","IFsrmDerivedObjectsResult::get_Results","Results property [File Server Resource Manager]","Results property [File Server Resource Manager]","IFsrmDerivedObjectsResult interface","fs.ifsrmderivedobjectsresult_results","fsrm.ifsrmderivedobjectsresult_results","fsrm/IFsrmDerivedObjectsResult::Results","fsrm/IFsrmDerivedObjectsResult::get_Results","get_Results"]
old-location: fsrm\ifsrmderivedobjectsresult_results.htm
tech.root: fsrm
ms.assetid: b5946160-565b-4c94-ba2e-18f270eb1af1
ms.date: 12/05/2018
ms.keywords: IFsrmDerivedObjectsResult interface [File Server Resource Manager],Results property, IFsrmDerivedObjectsResult.Results, IFsrmDerivedObjectsResult.get_Results, IFsrmDerivedObjectsResult::Results, IFsrmDerivedObjectsResult::get_Results, Results property [File Server Resource Manager], Results property [File Server Resource Manager],IFsrmDerivedObjectsResult interface, fs.ifsrmderivedobjectsresult_results, fsrm.ifsrmderivedobjectsresult_results, fsrm/IFsrmDerivedObjectsResult::Results, fsrm/IFsrmDerivedObjectsResult::get_Results, get_Results
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmScreen.h
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
 - IFsrmDerivedObjectsResult::get_Results
 - fsrm/IFsrmDerivedObjectsResult::get_Results
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
 - IFsrmDerivedObjectsResult.Results
 - IFsrmDerivedObjectsResult.get_Results
---

# IFsrmDerivedObjectsResult::get_Results


## -description

Retrieves the <b>HRESULT</b> values that indicate the success or failure of the update for each derived object.

This property is read-only.

## -parameters

## -remarks

The <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_derivedobjects">IFsrmDerivedObjectsResult::DerivedObjects</a> property contains the corresponding list of derived objects.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/updating-a-file-screen">Updating a File Screen</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmderivedobjectsresult">IFsrmDerivedObjectsResult</a>