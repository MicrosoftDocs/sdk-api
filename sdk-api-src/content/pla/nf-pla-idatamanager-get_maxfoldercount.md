---
UID: NF:pla.IDataManager.get_MaxFolderCount
title: IDataManager::get_MaxFolderCount
author: windows-sdk-content
description: Retrieves or sets the maximum number of folders to be used by all data collectors in the set.
old-location: pla\idatamanager_maxfoldercount.htm
old-project: PLA
ms.assetid: 71368635-e8c3-44fd-9d8a-f225b10225ba
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDataManager interface [PLA],MaxFolderCount property, IDataManager.MaxFolderCount, IDataManager.get_MaxFolderCount, IDataManager::MaxFolderCount, IDataManager::get_MaxFolderCount, IDataManager::put_MaxFolderCount, MaxFolderCount property [PLA], MaxFolderCount property [PLA],IDataManager interface, base.idatamanager_maxfoldercount, get_MaxFolderCount, pla.idatamanager_maxfoldercount, pla/IDataManager::MaxFolderCount, pla/IDataManager::get_MaxFolderCount, pla/IDataManager::put_MaxFolderCount
ms.prod: windows
ms.technology: windows-sdk
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
-	IDataManager.MaxFolderCount
-	IDataManager.get_MaxFolderCount
-	IDataManager.put_MaxFolderCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IDataManager::get_MaxFolderCount


## -description


Retrieves or sets the maximum number of folders to be used by all data collectors in the set. 

This property is read/write.


## -parameters


## -remarks



The maximum value applies to all subfolders under the path specified by the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a> property. The <a href="https://msdn.microsoft.com/23c7aced-d159-4d5e-a9ff-f0ca5b3e4470">IDataManager::CheckBeforeRunning</a> property checks this limit. The data manager also checks the limit when it runs.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

