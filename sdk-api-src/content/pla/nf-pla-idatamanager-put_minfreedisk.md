---
UID: NF:pla.IDataManager.put_MinFreeDisk
title: IDataManager::put_MinFreeDisk
author: windows-sdk-content
description: Retrieves or sets the minimum free disk space that needs to exist before data collection begins.
old-location: pla\idatamanager_minfreedisk.htm
tech.root: pla
ms.assetid: e5f4f752-ae96-4a1b-99a4-ff3b73fe3743
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDataManager interface [PLA],MinFreeDisk property, IDataManager.MinFreeDisk, IDataManager.put_MinFreeDisk, IDataManager::MinFreeDisk, IDataManager::get_MinFreeDisk, IDataManager::put_MinFreeDisk, MinFreeDisk property [PLA], MinFreeDisk property [PLA],IDataManager interface, base.idatamanager_minfreedisk, pla.idatamanager_minfreedisk, pla/IDataManager::MinFreeDisk, pla/IDataManager::get_MinFreeDisk, pla/IDataManager::put_MinFreeDisk, put_MinFreeDisk
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
req.lib: 
req.dll: Pla.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataManager::put_MinFreeDisk


## -description


Retrieves or sets the minimum free disk space that needs to exist before data collection begins.

This property is read/write.


## -parameters


## -remarks



The minimum value applies to the folder specified in the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a> property. The <a href="https://msdn.microsoft.com/23c7aced-d159-4d5e-a9ff-f0ca5b3e4470">IDataManager::CheckBeforeRunning</a> property checks this limit. The data manager also checks the limit when it runs.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

