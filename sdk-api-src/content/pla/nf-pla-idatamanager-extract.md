---
UID: NF:pla.IDataManager.Extract
title: IDataManager::Extract (pla.h)
description: Extracts the specified CAB file.
helpviewer_keywords: ["Extract","Extract method [PLA]","Extract method [PLA]","IDataManager interface","IDataManager interface [PLA]","Extract method","IDataManager.Extract","IDataManager::Extract","pla.idatamanager_extract","pla/IDataManager::Extract"]
old-location: pla\idatamanager_extract.htm
tech.root: PLA
ms.assetid: 73f5ca4c-6e7d-491e-a977-d41b7b69ff8c
ms.date: 12/05/2018
ms.keywords: Extract, Extract method [PLA], Extract method [PLA],IDataManager interface, IDataManager interface [PLA],Extract method, IDataManager.Extract, IDataManager::Extract, pla.idatamanager_extract, pla/IDataManager::Extract
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
 - IDataManager::Extract
 - pla/IDataManager::Extract
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
 - IDataManager.Extract
---

# IDataManager::Extract


## -description

Extracts the specified CAB file.

## -parameters

### -param CabFilename [in]

The name of the CAB file to extract.

### -param DestinationPath [in]

The path where you want to place the CAB file.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ifolderaction-get_actions">IFolderAction::Actions</a>