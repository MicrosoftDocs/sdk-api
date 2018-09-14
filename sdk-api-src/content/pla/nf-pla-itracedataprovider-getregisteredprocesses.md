---
UID: NF:pla.ITraceDataProvider.GetRegisteredProcesses
title: ITraceDataProvider::GetRegisteredProcesses
author: windows-sdk-content
description: Retrieves a list of processes that have registered as an Event Tracing for Windows (ETW) provider.
old-location: pla\itracedataprovider_getregisteredprocesses.htm
tech.root: PLA
ms.assetid: f848f209-c761-41aa-8e9f-4b7e2ecb54ae
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetRegisteredProcesses, GetRegisteredProcesses method [PLA], GetRegisteredProcesses method [PLA],ITraceDataProvider interface, ITraceDataProvider interface [PLA],GetRegisteredProcesses method, ITraceDataProvider.GetRegisteredProcesses, ITraceDataProvider::GetRegisteredProcesses, pla.itracedataprovider_getregisteredprocesses, pla/ITraceDataProvider::GetRegisteredProcesses
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
 - ITraceDataProvider.GetRegisteredProcesses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceDataProvider::GetRegisteredProcesses


## -description


Retrieves a list of processes that have registered as an Event Tracing for Windows (ETW) provider.


## -parameters




### -param Processes [out]

An <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface that contains the list of processes that have registered as an ETW provider. The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property  contains the name of the binary, and the <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the process identifier.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>
 

 

