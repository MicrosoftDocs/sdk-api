---
UID: NF:pla.IDataManager.Run
title: IDataManager::Run (pla.h)
description: Manually runs the data manager.
helpviewer_keywords: ["IDataManager interface [PLA]","Run method","IDataManager.Run","IDataManager::Run","Run","Run method [PLA]","Run method [PLA]","IDataManager interface","base.idatamanager_run","pla.idatamanager_run","pla/IDataManager::Run"]
old-location: pla\idatamanager_run.htm
tech.root: PLA
ms.assetid: a1016784-8841-485f-885e-3719bdb0ae05
ms.date: 12/05/2018
ms.keywords: IDataManager interface [PLA],Run method, IDataManager.Run, IDataManager::Run, Run, Run method [PLA], Run method [PLA],IDataManager interface, base.idatamanager_run, pla.idatamanager_run, pla/IDataManager::Run
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
 - IDataManager::Run
 - pla/IDataManager::Run
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
 - IDataManager.Run
---

# IDataManager::Run


## -description

Manually runs the data manager.

## -parameters

### -param Steps [in]

Determines whether the folder actions and resource policies are applied and how to generate the report. For possible steps, see the <a href="/windows/win32/api/pla/ne-pla-datamanagersteps">DataManagerSteps</a> enumeration.

### -param bstrFolder [in]

The folder under the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a> property that contains the files used to generate the report. If <b>NULL</b>, PLA uses all the files in the collection. This folder is used only if the <i>Steps</i> parameter includes <b>plaCreateReport</b> or <b>plaRunRules</b>.

### -param Errors [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface that you use to retrieve any errors that occurred. The value map can contain the list of directories where errors were encountered, along with the error codes. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_count">IValueMap::Count</a> property is zero if there were no errors.

## -returns

Returns S_OK if successful.

## -remarks

Data management runs in the current process and blocks until the data management steps complete.

To automatically run the data manager when the data collector set finishes running, set the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_enabled">IDataManager::Enabled</a> property to VARIANT_TRUE.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>