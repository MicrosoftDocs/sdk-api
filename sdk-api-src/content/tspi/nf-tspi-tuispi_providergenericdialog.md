---
UID: NF:tspi.TUISPI_providerGenericDialog
title: TUISPI_providerGenericDialog function (tspi.h)
description: The TUISPI_providerGenericDialog function in the UI DLL is called when the service provider sends a LINE_CREATEDIALOGINSTANCE message.
helpviewer_keywords: ["TUISPI_providerGenericDialog","TUISPI_providerGenericDialog function [TAPI 2.2]","_tspi_tuispi_providergenericdialog","tspi.tuispi_providergenericdialog","tspi/TUISPI_providerGenericDialog"]
old-location: tspi\tuispi_providergenericdialog.htm
tech.root: tapi3
ms.assetid: 2615ad41-b9bb-4bd4-9cfa-26b3c3336bee
ms.date: 12/05/2018
ms.keywords: TUISPI_providerGenericDialog, TUISPI_providerGenericDialog function [TAPI 2.2], _tspi_tuispi_providergenericdialog, tspi.tuispi_providergenericdialog, tspi/TUISPI_providerGenericDialog
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TUISPI_providerGenericDialog
 - tspi/TUISPI_providerGenericDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TUISPI_providerGenericDialog
---

# TUISPI_providerGenericDialog function


## -description

The 
<b>TUISPI_providerGenericDialog</b> function in the UI DLL is called when the service provider sends a 
<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a> message. The service provider uses this to create dialog boxes in the application context in conjunction with the processing of particular asynchronous TSPI functions. This function is called from a thread created specifically for the purpose of displaying the dialog box. The UI DLL does not return from this function until the dialog box is destroyed.

Implementation is mandatory if the service provider associated with the UI DLL sends LINE_CREATEDIALOGINSTANCE messages to spontaneously create dialog boxes in the application context.

## -parameters

### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box.

### -param htDlgInst

The opaque identifier binding the association of this instance of the function to a particular request from the service provider. The UI DLL must include this parameter, along with TUISPI_OBJECT_DIALOGINSTANCE, in any call to 
<a href="/windows/desktop/api/tspi/nc-tspi-tuispidllcallback">TUISPIDLLCALLBACK</a> to request further data from or deliver data to the service provider.

### -param lpParams

Pointer to a memory area used to hold a parameter block. The contents of this parameter block are specific to the service provider and its associated UI DLL. The conveyance of data through this parameter block is one-way to the UI DLL; changes made to the parameter block are not reflected back in the service provider. Generally, this parameter block holds all information the UI DLL needs to initially display the dialog box.

### -param dwSize

The size in bytes of the parameter block. If the <i>lpParams</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.

### -param hEvent

Handle to an event object created by TAPI. This event is signaled by the UI DLL through 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> (<i>hEvent</i>) when the UI DLL has completed initialization of this dialog box instance and is prepared to receive additional dialog box data through 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialogdata">TUISPI_providerGenericDialogData</a>. Data sent by the associated service provider (through 
<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a>) for this dialog box instance are blocked by TAPI until the UI DLL signals this event, giving 
<b>TUISPI_providerGenericDialog</b> the opportunity to perform any necessary initialization. The UI DLL should signal the event as quickly a possible to avoid blocking calls to 
<b>TUISPI_providerGenericDialogData</b>.

## -returns

Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a>



<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>



<a href="/windows/desktop/api/tspi/nc-tspi-tuispidllcallback">TUISPIDLLCALLBACK</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialogdata">TUISPI_providerGenericDialogData</a>