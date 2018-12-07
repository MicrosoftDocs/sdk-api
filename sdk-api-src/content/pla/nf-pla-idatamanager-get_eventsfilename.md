---
UID: NF:pla.IDataManager.get_EventsFileName
title: IDataManager::get_EventsFileName
author: windows-sdk-content
description: Retrieves or sets the name for the events file.
old-location: pla\idatamanager_eventsfilename.htm
tech.root: pla
ms.assetid: ce67779a-3312-496f-a793-ac8720e63fb4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EventsFileName property [PLA], EventsFileName property [PLA],IDataManager interface, IDataManager interface [PLA],EventsFileName property, IDataManager.EventsFileName, IDataManager.get_EventsFileName, IDataManager::EventsFileName, IDataManager::get_EventsFileName, IDataManager::put_EventsFileName, base.idatamanager_eventsfilename, get_EventsFileName, pla.idatamanager_eventsfilename, pla/IDataManager::EventsFileName, pla/IDataManager::get_EventsFileName, pla/IDataManager::put_EventsFileName
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
 - IDataManager.EventsFileName
 - IDataManager.get_EventsFileName
 - IDataManager.put_EventsFileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataManager::get_EventsFileName


## -description


Retrieves or sets the name for the events file. 

This property is read/write.


## -parameters


## -remarks



PLA uses the file name only if you include the <b>plaCreateReport</b> value of the <a href="https://msdn.microsoft.com/e647987d-e524-475e-a355-539cb3f04635">DataManagerSteps</a> enumeration in the <i>Steps</i> parameter of the <a href="https://msdn.microsoft.com/a1016784-8841-485f-885e-3719bdb0ae05">IDataManager::Run</a> method and if the data collection set contains trace data collectors.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

