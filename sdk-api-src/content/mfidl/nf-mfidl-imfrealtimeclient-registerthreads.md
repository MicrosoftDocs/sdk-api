---
UID: NF:mfidl.IMFRealTimeClient.RegisterThreads
title: IMFRealTimeClient::RegisterThreads
author: windows-sdk-content
description: Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfrealtimeclient_registerthreads.htm
old-project: medfound
ms.assetid: 0ed3a8f6-1ea1-44af-ac6e-8712fd59ae31
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 0ed3a8f6-1ea1-44af-ac6e-8712fd59ae31, IMFRealTimeClient interface [Media Foundation],RegisterThreads method, IMFRealTimeClient.RegisterThreads, IMFRealTimeClient::RegisterThreads, RegisterThreads, RegisterThreads method [Media Foundation], RegisterThreads method [Media Foundation],IMFRealTimeClient interface, mf.imfrealtimeclient_registerthreads, mfidl/IMFRealTimeClient::RegisterThreads
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRealTimeClient.RegisterThreads
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFRealTimeClient::RegisterThreads


## -description


Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS).


## -parameters




### -param dwTaskIndex [in]


            The MMCSS task identifier.
          


### -param wszClass [in]

The name of the MMCSS task.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The object's worker threads should register themselves with MMCSS by calling <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a>, using the task name and identifier specified in this method.




## -see-also




<a href="https://msdn.microsoft.com/b1d1901e-dd49-421f-9212-61e32cff411e">IMFRealTimeClient</a>
 

 

