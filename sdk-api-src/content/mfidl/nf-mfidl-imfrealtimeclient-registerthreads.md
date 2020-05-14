---
UID: NF:mfidl.IMFRealTimeClient.RegisterThreads
title: IMFRealTimeClient::RegisterThreads (mfidl.h)
description: Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS).helpviewer_keywords: ["0ed3a8f6-1ea1-44af-ac6e-8712fd59ae31","IMFRealTimeClient interface [Media Foundation]","RegisterThreads method","IMFRealTimeClient.RegisterThreads","IMFRealTimeClient::RegisterThreads","RegisterThreads","RegisterThreads method [Media Foundation]","RegisterThreads method [Media Foundation]","IMFRealTimeClient interface","mf.imfrealtimeclient_registerthreads","mfidl/IMFRealTimeClient::RegisterThreads"]
old-location: mf\imfrealtimeclient_registerthreads.htm
tech.root: medfound
ms.assetid: 0ed3a8f6-1ea1-44af-ac6e-8712fd59ae31
ms.date: 12/05/2018
ms.keywords: 0ed3a8f6-1ea1-44af-ac6e-8712fd59ae31, IMFRealTimeClient interface [Media Foundation],RegisterThreads method, IMFRealTimeClient.RegisterThreads, IMFRealTimeClient::RegisterThreads, RegisterThreads, RegisterThreads method [Media Foundation], RegisterThreads method [Media Foundation],IMFRealTimeClient interface, mf.imfrealtimeclient_registerthreads, mfidl/IMFRealTimeClient::RegisterThreads
f1_keywords:
- mfidl/IMFRealTimeClient.RegisterThreads
dev_langs:
- c++
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The object's worker threads should register themselves with MMCSS by calling <a href="https://docs.microsoft.com/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a>, using the task name and identifier specified in this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient">IMFRealTimeClient</a>
 

 

