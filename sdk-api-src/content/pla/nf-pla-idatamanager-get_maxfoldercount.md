---
UID: NF:pla.IDataManager.get_MaxFolderCount
title: IDataManager::get_MaxFolderCount (pla.h)
description: Retrieves or sets the maximum number of folders to be used by all data collectors in the set. (Get)
helpviewer_keywords: ["IDataManager interface [PLA]","MaxFolderCount property","IDataManager.MaxFolderCount","IDataManager.get_MaxFolderCount","IDataManager::MaxFolderCount","IDataManager::get_MaxFolderCount","IDataManager::put_MaxFolderCount","MaxFolderCount property [PLA]","MaxFolderCount property [PLA]","IDataManager interface","base.idatamanager_maxfoldercount","get_MaxFolderCount","pla.idatamanager_maxfoldercount","pla/IDataManager::MaxFolderCount","pla/IDataManager::get_MaxFolderCount","pla/IDataManager::put_MaxFolderCount"]
old-location: pla\idatamanager_maxfoldercount.htm
tech.root: PLA
ms.assetid: 71368635-e8c3-44fd-9d8a-f225b10225ba
ms.date: 12/05/2018
ms.keywords: IDataManager interface [PLA],MaxFolderCount property, IDataManager.MaxFolderCount, IDataManager.get_MaxFolderCount, IDataManager::MaxFolderCount, IDataManager::get_MaxFolderCount, IDataManager::put_MaxFolderCount, MaxFolderCount property [PLA], MaxFolderCount property [PLA],IDataManager interface, base.idatamanager_maxfoldercount, get_MaxFolderCount, pla.idatamanager_maxfoldercount, pla/IDataManager::MaxFolderCount, pla/IDataManager::get_MaxFolderCount, pla/IDataManager::put_MaxFolderCount
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
 - IDataManager::get_MaxFolderCount
 - pla/IDataManager::get_MaxFolderCount
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
 - IDataManager.MaxFolderCount
 - IDataManager.get_MaxFolderCount
 - IDataManager.put_MaxFolderCount
---

# IDataManager::get_MaxFolderCount


## -description

Retrieves or sets the maximum number of folders to be used by all data collectors in the set. 

This property is read/write.

## -parameters

## -remarks

The maximum value applies to all subfolders under the path specified by the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a> property. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_checkbeforerunning">IDataManager::CheckBeforeRunning</a> property checks this limit. The data manager also checks the limit when it runs.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>
