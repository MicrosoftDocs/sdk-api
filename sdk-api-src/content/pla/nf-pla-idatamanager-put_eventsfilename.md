---
UID: NF:pla.IDataManager.put_EventsFileName
title: IDataManager::put_EventsFileName (pla.h)
author: windows-sdk-content
description: Retrieves or sets the name for the events file.
old-location: pla\idatamanager_eventsfilename.htm
tech.root: PLA
ms.assetid: ce67779a-3312-496f-a793-ac8720e63fb4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventsFileName property [PLA], EventsFileName property [PLA],IDataManager interface, IDataManager interface [PLA],EventsFileName property, IDataManager.EventsFileName, IDataManager.put_EventsFileName, IDataManager::EventsFileName, IDataManager::get_EventsFileName, IDataManager::put_EventsFileName, base.idatamanager_eventsfilename, pla.idatamanager_eventsfilename, pla/IDataManager::EventsFileName, pla/IDataManager::get_EventsFileName, pla/IDataManager::put_EventsFileName, put_EventsFileName
ms.topic: method
f1_keywords: 
 - "pla/IDataManager.EventsFileName"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataManager::put_EventsFileName


## -description


Retrieves or sets the name for the events file. 

This property is read/write.


## -parameters


## -remarks



PLA uses the file name only if you include the <b>plaCreateReport</b> value of the <a href="https://docs.microsoft.com/windows/win32/api/pla/ne-pla-datamanagersteps">DataManagerSteps</a> enumeration in the <i>Steps</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-run">IDataManager::Run</a> method and if the data collection set contains trace data collectors.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>
 

 

