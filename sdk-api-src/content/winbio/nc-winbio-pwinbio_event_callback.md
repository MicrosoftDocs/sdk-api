---
UID: NC:winbio.PWINBIO_EVENT_CALLBACK
title: PWINBIO_EVENT_CALLBACK (winbio.h)
description: Returns results from the asynchronous WinBioRegisterEventMonitor function.
helpviewer_keywords: ["PWINBIO_EVENT_CALLBACK","PWINBIO_EVENT_CALLBACK callback","PWINBIO_EVENT_CALLBACK callback function [Windows Biometric Framework API]","secbiomet.pwinbio_event_callback","winbio/PWINBIO_EVENT_CALLBACK"]
old-location: secbiomet\pwinbio_event_callback.htm
tech.root: SecBioMet
ms.assetid: E5D3E20E-A174-46E2-9426-7B021496DB3B
ms.date: 12/05/2018
ms.keywords: PWINBIO_EVENT_CALLBACK, PWINBIO_EVENT_CALLBACK callback, PWINBIO_EVENT_CALLBACK callback function [Windows Biometric Framework API], secbiomet.pwinbio_event_callback, winbio/PWINBIO_EVENT_CALLBACK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWINBIO_EVENT_CALLBACK
 - winbio/PWINBIO_EVENT_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio.h
api_name:
 - PWINBIO_EVENT_CALLBACK
---

# PWINBIO_EVENT_CALLBACK callback function


## -description

Called by the Windows Biometric Framework to return results from the   asynchronous  <a href="/windows/desktop/api/winbio/nf-winbio-winbioregistereventmonitor">WinBioRegisterEventMonitor</a> function. The client application must implement this function.

## -parameters

### -param EventCallbackContext [in, optional]

Pointer to a buffer defined by the application and passed to the <i>EventCallbackContext</i> parameter of the <a href="/windows/desktop/api/winbio/nf-winbio-winbioregistereventmonitor">WinBioRegisterEventMonitor</a> function. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform or to maintain additional information about the biometric capture.

### -param OperationStatus [in]

Error code returned by the capture operation.

### -param Event [in]

Pointer to a WINBIO_EVENT value. For more information, see <a href="/windows/desktop/SecBioMet/winbio-event-constants">WINBIO_EVENT Constants</a>.