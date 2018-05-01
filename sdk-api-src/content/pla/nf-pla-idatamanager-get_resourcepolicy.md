---
UID: NF:pla.IDataManager.get_ResourcePolicy
title: IDataManager::get_ResourcePolicy method
author: windows-driver-content
description: Retrieves or sets the action to take when one of the disk resource limits is exceeded.
old-location: pla\idatamanager_resourcepolicy.htm
old-project: PLA
ms.assetid: 541cd28c-2e01-4b8a-9cd3-044896c8fb80
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDataManager, IDataManager interface [PLA], ResourcePolicy property, IDataManager.ResourcePolicy, IDataManager::get_ResourcePolicy, IDataManager::put_ResourcePolicy, ResourcePolicy property [PLA], ResourcePolicy property [PLA], IDataManager interface, base.idatamanager_resourcepolicy, get_ResourcePolicy,IDataManager.get_ResourcePolicy, pla.idatamanager_resourcepolicy, pla/IDataManager::ResourcePolicy, pla/IDataManager::get_ResourcePolicy, pla/IDataManager::put_ResourcePolicy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataManager.ResourcePolicy
-	IDataManager.get_ResourcePolicy
-	IDataManager.put_ResourcePolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataManager::get_ResourcePolicy method


## -description


Retrieves or sets the action to take when one of the disk resource limits is exceeded. 

This property is read/write.


## -parameters


## -remarks



The folders are deleted based on the resource policy until the disk resource condition is satisfied. For example, if the maximum size is 7 MB and the current size is 10 MB, PLA will delete folders until the current size is 7 MB or less. If the first folder to be deleted is 3 MB, PLA will delete that folder and then stop deleting folders because the current size will be equal to the maximum size. If the first folder to be deleted is 9 MB, PLA will delete that folder and then stop deleting folders because the current size will be 1 MB, which will also satisfy the condition.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>



<a href="https://msdn.microsoft.com/59fad3d2-9971-4608-8576-977d4dd8ace4">IDataManager::FolderActions</a>
 

 

