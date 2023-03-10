---
UID: NF:pla.IDataManager.get_ResourcePolicy
title: IDataManager::get_ResourcePolicy (pla.h)
description: Retrieves or sets the action to take when one of the disk resource limits is exceeded. (Get)
helpviewer_keywords: ["IDataManager interface [PLA]","ResourcePolicy property","IDataManager.ResourcePolicy","IDataManager.get_ResourcePolicy","IDataManager::ResourcePolicy","IDataManager::get_ResourcePolicy","IDataManager::put_ResourcePolicy","ResourcePolicy property [PLA]","ResourcePolicy property [PLA]","IDataManager interface","base.idatamanager_resourcepolicy","get_ResourcePolicy","pla.idatamanager_resourcepolicy","pla/IDataManager::ResourcePolicy","pla/IDataManager::get_ResourcePolicy","pla/IDataManager::put_ResourcePolicy"]
old-location: pla\idatamanager_resourcepolicy.htm
tech.root: PLA
ms.assetid: 541cd28c-2e01-4b8a-9cd3-044896c8fb80
ms.date: 12/05/2018
ms.keywords: IDataManager interface [PLA],ResourcePolicy property, IDataManager.ResourcePolicy, IDataManager.get_ResourcePolicy, IDataManager::ResourcePolicy, IDataManager::get_ResourcePolicy, IDataManager::put_ResourcePolicy, ResourcePolicy property [PLA], ResourcePolicy property [PLA],IDataManager interface, base.idatamanager_resourcepolicy, get_ResourcePolicy, pla.idatamanager_resourcepolicy, pla/IDataManager::ResourcePolicy, pla/IDataManager::get_ResourcePolicy, pla/IDataManager::put_ResourcePolicy
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
 - IDataManager::get_ResourcePolicy
 - pla/IDataManager::get_ResourcePolicy
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
 - IDataManager.ResourcePolicy
 - IDataManager.get_ResourcePolicy
 - IDataManager.put_ResourcePolicy
---

# IDataManager::get_ResourcePolicy


## -description

Retrieves or sets the action to take when one of the disk resource limits is exceeded. 

This property is read/write.

## -parameters

## -remarks

The folders are deleted based on the resource policy until the disk resource condition is satisfied. For example, if the maximum size is 7 MB and the current size is 10 MB, PLA will delete folders until the current size is 7 MB or less. If the first folder to be deleted is 3 MB, PLA will delete that folder and then stop deleting folders because the current size will be equal to the maximum size. If the first folder to be deleted is 9 MB, PLA will delete that folder and then stop deleting folders because the current size will be 1 MB, which will also satisfy the condition.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_folderactions">IDataManager::FolderActions</a>
