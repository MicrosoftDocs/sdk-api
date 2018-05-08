---
UID: NF:pla.IConfigurationDataCollector.put_SystemStateFile
title: IConfigurationDataCollector::put_SystemStateFile
author: windows-driver-content
description: Retrieves or sets the name of the file that contains the saved system state.
old-location: pla\iconfigurationdatacollector_systemstatefile.htm
old-project: PLA
ms.assetid: e8e4ec1f-4b43-4252-8a31-55b2ed2dca36
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IConfigurationDataCollector interface [PLA],SystemStateFile property, IConfigurationDataCollector.SystemStateFile, IConfigurationDataCollector.put_SystemStateFile, IConfigurationDataCollector::SystemStateFile, IConfigurationDataCollector::get_SystemStateFile, IConfigurationDataCollector::put_SystemStateFile, SystemStateFile property [PLA], SystemStateFile property [PLA],IConfigurationDataCollector interface, pla.iconfigurationdatacollector_systemstatefile, pla/IConfigurationDataCollector::SystemStateFile, pla/IConfigurationDataCollector::get_SystemStateFile, pla/IConfigurationDataCollector::put_SystemStateFile, put_SystemStateFile
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
-	IConfigurationDataCollector.SystemStateFile
-	IConfigurationDataCollector.get_SystemStateFile
-	IConfigurationDataCollector.put_SystemStateFile
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IConfigurationDataCollector::put_SystemStateFile


## -description


Retrieves or sets the name of the file that contains the saved system state.

This property is read/write.


## -parameters


## -remarks



Do not include the path in the file name; the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a> and <a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">IDataCollectorSet::Subdirectory</a> properties determine the path to the file.

If you do not specify the name of the file, the system state is not retrieved.

The state information is a snapshot of the Circular Kernel Context Logger. The context logger provides a snapshot of the current state of the computer. The file contains kernel events. You can use the TraceRpt.exe tool to decode the events.




## -see-also




<a href="https://msdn.microsoft.com/7266c02d-0f56-4754-8a67-68394a5f0158">IConfigurationDataCollector</a>
 

 

