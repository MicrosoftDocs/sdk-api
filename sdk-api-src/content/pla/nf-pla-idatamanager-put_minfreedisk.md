---
UID: NF:pla.IDataManager.put_MinFreeDisk
title: IDataManager::put_MinFreeDisk (pla.h)
description: Retrieves or sets the minimum free disk space that needs to exist before data collection begins. (Put)
helpviewer_keywords: ["IDataManager interface [PLA]","MinFreeDisk property","IDataManager.MinFreeDisk","IDataManager.put_MinFreeDisk","IDataManager::MinFreeDisk","IDataManager::get_MinFreeDisk","IDataManager::put_MinFreeDisk","MinFreeDisk property [PLA]","MinFreeDisk property [PLA]","IDataManager interface","base.idatamanager_minfreedisk","pla.idatamanager_minfreedisk","pla/IDataManager::MinFreeDisk","pla/IDataManager::get_MinFreeDisk","pla/IDataManager::put_MinFreeDisk","put_MinFreeDisk"]
old-location: pla\idatamanager_minfreedisk.htm
tech.root: PLA
ms.assetid: e5f4f752-ae96-4a1b-99a4-ff3b73fe3743
ms.date: 12/05/2018
ms.keywords: IDataManager interface [PLA],MinFreeDisk property, IDataManager.MinFreeDisk, IDataManager.put_MinFreeDisk, IDataManager::MinFreeDisk, IDataManager::get_MinFreeDisk, IDataManager::put_MinFreeDisk, MinFreeDisk property [PLA], MinFreeDisk property [PLA],IDataManager interface, base.idatamanager_minfreedisk, pla.idatamanager_minfreedisk, pla/IDataManager::MinFreeDisk, pla/IDataManager::get_MinFreeDisk, pla/IDataManager::put_MinFreeDisk, put_MinFreeDisk
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
 - IDataManager::put_MinFreeDisk
 - pla/IDataManager::put_MinFreeDisk
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
 - IDataManager.MinFreeDisk
 - IDataManager.get_MinFreeDisk
 - IDataManager.put_MinFreeDisk
---

# IDataManager::put_MinFreeDisk


## -description

Retrieves or sets the minimum free disk space that needs to exist before data collection begins.

This property is read/write.

## -parameters

## -remarks

The minimum value applies to the folder specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a> property. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_checkbeforerunning">IDataManager::CheckBeforeRunning</a> property checks this limit. The data manager also checks the limit when it runs.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>
