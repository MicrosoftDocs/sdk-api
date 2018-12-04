---
UID: NF:tspi.TUISPI_providerGenericDialogData
title: TUISPI_providerGenericDialogData function
author: windows-sdk-content
description: The TUISPI_providerGenericDialogData function in the UI DLL is called when the service provider sends a LINE_SENDDIALOGINSTANCEDATA message.
old-location: tspi\tuispi_providergenericdialogdata.htm
tech.root: tapi
ms.assetid: 212ae478-49e1-44ce-b589-f2fb3994a2a2
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: TUISPI_providerGenericDialogData, TUISPI_providerGenericDialogData function [TAPI 2.2], _tspi_tuispi_providergenericdialogdata, tspi.tuispi_providergenericdialogdata, tspi/TUISPI_providerGenericDialogData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TUISPI_providerGenericDialogData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TUISPI_providerGenericDialogData function


## -description


The 
<b>TUISPI_providerGenericDialogData</b> function in the UI DLL is called when the service provider sends a 
<a href="https://msdn.microsoft.com/d3c176ba-8b4b-4b7c-a603-130dfa761898">LINE_SENDDIALOGINSTANCEDATA</a> message. The service provider uses this to spontaneously update information in dialog boxes created in the application context in conjunction with the processing of particular asynchronous TSPI functions. This function is called from a separate thread from that in which 
<b>TUISPI_providerGenericDialogData</b> is executing. The UI DLL should not block the thread in which this function is called, but should process the data and return immediately (posting a message to the dialog box if necessary).

Implementation is mandatory if 
<a href="https://msdn.microsoft.com/2615ad41-b9bb-4bd4-9cfa-26b3c3336bee">TUISPI_providerGenericDialog</a> is exported.


## -parameters




### -param htDlgInst

The opaque identifier binding the association of this instance of the function to a particular request from the service provider.


### -param lpParams

Pointer to a memory area used to hold a parameter block. The contents of this parameter block are specific to the service provider and its associated UI DLL. The conveyance of data through this parameter block is one-way to the UI DLL; changes made to the parameter block are not reflected back in the service provider. If this parameter is set to <b>NULL</b>, this is a request to close the dialog box immediately and clean up (
<a href="https://msdn.microsoft.com/2f4ec748-26ff-49c5-bd88-6c6e64e5bc89">TUISPIDLLCALLBACK</a> should not be invoked during this cleanup). TAPI invokes this function with <i>lpParams</i> set to <b>NULL</b> to force dialog box cleanup under certain circumstances, such as an application calling 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a> with a dialog box still active.


### -param dwSize

The size in bytes of the parameter block. If the <i>lpParams</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.
					


## -returns



Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.




## -see-also




<a href="https://msdn.microsoft.com/d3c176ba-8b4b-4b7c-a603-130dfa761898">LINE_SENDDIALOGINSTANCEDATA</a>



<a href="https://msdn.microsoft.com/2f4ec748-26ff-49c5-bd88-6c6e64e5bc89">TUISPIDLLCALLBACK</a>



<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a>
 

 

