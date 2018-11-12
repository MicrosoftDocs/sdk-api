---
UID: NF:tspi.TUISPI_providerGenericDialog
title: TUISPI_providerGenericDialog function
author: windows-sdk-content
description: The TUISPI_providerGenericDialog function in the UI DLL is called when the service provider sends a LINE_CREATEDIALOGINSTANCE message.
old-location: tspi\tuispi_providergenericdialog.htm
tech.root: tapi
ms.assetid: 2615ad41-b9bb-4bd4-9cfa-26b3c3336bee
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: TUISPI_providerGenericDialog, TUISPI_providerGenericDialog function [TAPI 2.2], _tspi_tuispi_providergenericdialog, tspi.tuispi_providergenericdialog, tspi/TUISPI_providerGenericDialog
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
 - TUISPI_providerGenericDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TUISPI_providerGenericDialog function


## -description


The 
<b>TUISPI_providerGenericDialog</b> function in the UI DLL is called when the service provider sends a 
<a href="https://msdn.microsoft.com/5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75">LINE_CREATEDIALOGINSTANCE</a> message. The service provider uses this to create dialog boxes in the application context in conjunction with the processing of particular asynchronous TSPI functions. This function is called from a thread created specifically for the purpose of displaying the dialog box. The UI DLL does not return from this function until the dialog box is destroyed.

Implementation is mandatory if the service provider associated with the UI DLL sends LINE_CREATEDIALOGINSTANCE messages to spontaneously create dialog boxes in the application context.


## -parameters




### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box.


### -param htDlgInst

The opaque identifier binding the association of this instance of the function to a particular request from the service provider. The UI DLL must include this parameter, along with TUISPI_OBJECT_DIALOGINSTANCE, in any call to 
<a href="https://msdn.microsoft.com/2f4ec748-26ff-49c5-bd88-6c6e64e5bc89">TUISPIDLLCALLBACK</a> to request further data from or deliver data to the service provider.


### -param lpParams

Pointer to a memory area used to hold a parameter block. The contents of this parameter block are specific to the service provider and its associated UI DLL. The conveyance of data through this parameter block is one-way to the UI DLL; changes made to the parameter block are not reflected back in the service provider. Generally, this parameter block holds all information the UI DLL needs to initially display the dialog box.


### -param dwSize

The size in bytes of the parameter block. If the <i>lpParams</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.


### -param hEvent

Handle to an event object created by TAPI. This event is signaled by the UI DLL through 
<a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a> (<i>hEvent</i>) when the UI DLL has completed initialization of this dialog box instance and is prepared to receive additional dialog box data through 
<a href="https://msdn.microsoft.com/212ae478-49e1-44ce-b589-f2fb3994a2a2">TUISPI_providerGenericDialogData</a>. Data sent by the associated service provider (through 
<a href="https://msdn.microsoft.com/d3c176ba-8b4b-4b7c-a603-130dfa761898">LINE_SENDDIALOGINSTANCEDATA</a>) for this dialog box instance are blocked by TAPI until the UI DLL signals this event, giving 
<b>TUISPI_providerGenericDialog</b> the opportunity to perform any necessary initialization. The UI DLL should signal the event as quickly a possible to avoid blocking calls to 
<b>TUISPI_providerGenericDialogData</b>.


## -returns



Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.




## -see-also




<a href="https://msdn.microsoft.com/5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75">LINE_CREATEDIALOGINSTANCE</a>



<a href="https://msdn.microsoft.com/d3c176ba-8b4b-4b7c-a603-130dfa761898">LINE_SENDDIALOGINSTANCEDATA</a>



<a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a>



<a href="https://msdn.microsoft.com/2f4ec748-26ff-49c5-bd88-6c6e64e5bc89">TUISPIDLLCALLBACK</a>



<a href="https://msdn.microsoft.com/212ae478-49e1-44ce-b589-f2fb3994a2a2">TUISPI_providerGenericDialogData</a>
 

 

