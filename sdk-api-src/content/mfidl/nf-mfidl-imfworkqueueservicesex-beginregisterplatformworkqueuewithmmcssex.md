---
UID: NF:mfidl.IMFWorkQueueServicesEx.BeginRegisterPlatformWorkQueueWithMMCSSEx
title: IMFWorkQueueServicesEx::BeginRegisterPlatformWorkQueueWithMMCSSEx
author: windows-sdk-content
description: Registers a platform work queue with Multimedia Class Scheduler Service (MMCSS) using the specified class and task id.
old-location: mf\imfworkqueueservicesex_beginregisterplatformworkqueuewithmmcssex.htm
old-project: medfound
ms.assetid: 761e0e51-06e9-4b26-b6ad-afeaa7150e64
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: BeginRegisterPlatformWorkQueueWithMMCSSEx, BeginRegisterPlatformWorkQueueWithMMCSSEx method [Media Foundation], BeginRegisterPlatformWorkQueueWithMMCSSEx method [Media Foundation],IMFWorkQueueServicesEx interface, IMFWorkQueueServicesEx interface [Media Foundation],BeginRegisterPlatformWorkQueueWithMMCSSEx method, IMFWorkQueueServicesEx.BeginRegisterPlatformWorkQueueWithMMCSSEx, IMFWorkQueueServicesEx::BeginRegisterPlatformWorkQueueWithMMCSSEx, mf.imfworkqueueservicesex_beginregisterplatformworkqueuewithmmcssex, mfidl/IMFWorkQueueServicesEx::BeginRegisterPlatformWorkQueueWithMMCSSEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - mfidl.h
api_name:
 - IMFWorkQueueServicesEx.BeginRegisterPlatformWorkQueueWithMMCSSEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFWorkQueueServicesEx::BeginRegisterPlatformWorkQueueWithMMCSSEx


## -description


Registers a platform work queue with Multimedia Class Scheduler Service (MMCSS) using the specified
    class and task id.


## -parameters




### -param dwPlatformWorkQueue [in]

The id of one of the standard platform work queues.


### -param wszClass [in]

The MMCSS class which the work queue should be registered with.


### -param dwTaskId [in]

    The task id which the work queue should be registered with. If <i>dwTaskId</i> is 0, a new MMCSS bucket will be created.


### -param lPriority [in]

The priority.


### -param pCallback [in]

Standard callback used for async operations in Media Foundation.


### -param pState [in]

Standard state used for async operations in Media Foundation.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/12d4f0f4-9a6d-4782-b5ae-4add6608782a">IMFWorkQueueServicesEx</a>
 

 

