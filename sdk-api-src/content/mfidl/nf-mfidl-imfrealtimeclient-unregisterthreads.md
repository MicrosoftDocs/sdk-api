---
UID: NF:mfidl.IMFRealTimeClient.UnregisterThreads
title: IMFRealTimeClient::UnregisterThreads
author: windows-sdk-content
description: Notifies the object to unregister its worker threads from the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfrealtimeclient_unregisterthreads.htm
tech.root: medfound
ms.assetid: 9bd65ff1-c283-47b8-8299-383b2b773c18
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 9bd65ff1-c283-47b8-8299-383b2b773c18, IMFRealTimeClient interface [Media Foundation],UnregisterThreads method, IMFRealTimeClient.UnregisterThreads, IMFRealTimeClient::UnregisterThreads, UnregisterThreads, UnregisterThreads method [Media Foundation], UnregisterThreads method [Media Foundation],IMFRealTimeClient interface, mf.imfrealtimeclient_unregisterthreads, mfidl/IMFRealTimeClient::UnregisterThreads
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFRealTimeClient.UnregisterThreads
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFRealTimeClient::UnregisterThreads


## -description


Notifies the object to unregister its worker threads from the Multimedia Class Scheduler Service (MMCSS).
        


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The object's worker threads should unregister themselves from MMCSS by calling <a href="https://msdn.microsoft.com/2ae0d34c-3819-46fa-9779-5de8a57e5281">AvRevertMmThreadCharacteristics</a>.




## -see-also




<a href="https://msdn.microsoft.com/b1d1901e-dd49-421f-9212-61e32cff411e">IMFRealTimeClient</a>
 

 

