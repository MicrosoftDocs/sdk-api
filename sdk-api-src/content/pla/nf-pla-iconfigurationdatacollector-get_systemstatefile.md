---
UID: NF:pla.IConfigurationDataCollector.get_SystemStateFile
title: IConfigurationDataCollector::get_SystemStateFile (pla.h)
description: Retrieves or sets the name of the file that contains the saved system state. (Get)
helpviewer_keywords: ["IConfigurationDataCollector interface [PLA]","SystemStateFile property","IConfigurationDataCollector.SystemStateFile","IConfigurationDataCollector.get_SystemStateFile","IConfigurationDataCollector::SystemStateFile","IConfigurationDataCollector::get_SystemStateFile","IConfigurationDataCollector::put_SystemStateFile","SystemStateFile property [PLA]","SystemStateFile property [PLA]","IConfigurationDataCollector interface","get_SystemStateFile","pla.iconfigurationdatacollector_systemstatefile","pla/IConfigurationDataCollector::SystemStateFile","pla/IConfigurationDataCollector::get_SystemStateFile","pla/IConfigurationDataCollector::put_SystemStateFile"]
old-location: pla\iconfigurationdatacollector_systemstatefile.htm
tech.root: PLA
ms.assetid: e8e4ec1f-4b43-4252-8a31-55b2ed2dca36
ms.date: 12/05/2018
ms.keywords: IConfigurationDataCollector interface [PLA],SystemStateFile property, IConfigurationDataCollector.SystemStateFile, IConfigurationDataCollector.get_SystemStateFile, IConfigurationDataCollector::SystemStateFile, IConfigurationDataCollector::get_SystemStateFile, IConfigurationDataCollector::put_SystemStateFile, SystemStateFile property [PLA], SystemStateFile property [PLA],IConfigurationDataCollector interface, get_SystemStateFile, pla.iconfigurationdatacollector_systemstatefile, pla/IConfigurationDataCollector::SystemStateFile, pla/IConfigurationDataCollector::get_SystemStateFile, pla/IConfigurationDataCollector::put_SystemStateFile
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
 - IConfigurationDataCollector::get_SystemStateFile
 - pla/IConfigurationDataCollector::get_SystemStateFile
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
 - IConfigurationDataCollector.SystemStateFile
 - IConfigurationDataCollector.get_SystemStateFile
 - IConfigurationDataCollector.put_SystemStateFile
---

# IConfigurationDataCollector::get_SystemStateFile


## -description

Retrieves or sets the name of the file that contains the saved system state.

This property is read/write.

## -parameters

## -remarks

Do not include the path in the file name; the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectory">IDataCollectorSet::Subdirectory</a> properties determine the path to the file.

If you do not specify the name of the file, the system state is not retrieved.

The state information is a snapshot of the Circular Kernel Context Logger. The context logger provides a snapshot of the current state of the computer. The file contains kernel events. You can use the TraceRpt.exe tool to decode the events.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iconfigurationdatacollector">IConfigurationDataCollector</a>
