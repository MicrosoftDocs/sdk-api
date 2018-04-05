---
UID: NC:winbio.PWINBIO_EVENT_CALLBACK
title: PWINBIO_EVENT_CALLBACK
author: windows-driver-content
description: Returns results from the asynchronous WinBioRegisterEventMonitor function.
old-location: secbiomet\pwinbio_event_callback.htm
old-project: SecBioMet
ms.assetid: E5D3E20E-A174-46E2-9426-7B021496DB3B
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PWINBIO_EVENT_CALLBACK, PWINBIO_EVENT_CALLBACK callback function [Windows Biometric Framework API], secbiomet.pwinbio_event_callback, winbio/PWINBIO_EVENT_CALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winbio.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio.h
api_name:
-	PWINBIO_EVENT_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PWINBIO_EVENT_CALLBACK callback


## -description


Called by the Windows Biometric Framework to return results from the   asynchronous  <a href="https://msdn.microsoft.com/408291ca-66fe-4f4a-8f6e-3a1b60eb2d15">WinBioRegisterEventMonitor</a> function. The client application must implement this function.


## -parameters




### -param EventCallbackContext [in, optional]

Pointer to a buffer defined by the application and passed to the <i>EventCallbackContext</i> parameter of the <a href="https://msdn.microsoft.com/408291ca-66fe-4f4a-8f6e-3a1b60eb2d15">WinBioRegisterEventMonitor</a> function. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform or to maintain additional information about the biometric capture.


### -param OperationStatus [in]

Error code returned by the capture operation.


### -param Event [in]

Pointer to a WINBIO_EVENT value. For more information, see <a href="https://msdn.microsoft.com/73805413-a8d9-4682-aa21-7032451d750a">WINBIO_EVENT Constants</a>.


## -returns



Do not return a value from your implementation of this function.



