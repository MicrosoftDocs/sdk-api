---
UID: NF:tspi.TUISPI_providerGenericDialogData
title: TUISPI_providerGenericDialogData function (tspi.h)
description: The TUISPI_providerGenericDialogData function in the UI DLL is called when the service provider sends a LINE_SENDDIALOGINSTANCEDATA message.
helpviewer_keywords: ["TUISPI_providerGenericDialogData","TUISPI_providerGenericDialogData function [TAPI 2.2]","_tspi_tuispi_providergenericdialogdata","tspi.tuispi_providergenericdialogdata","tspi/TUISPI_providerGenericDialogData"]
old-location: tspi\tuispi_providergenericdialogdata.htm
tech.root: tapi3
ms.assetid: 212ae478-49e1-44ce-b589-f2fb3994a2a2
ms.date: 12/05/2018
ms.keywords: TUISPI_providerGenericDialogData, TUISPI_providerGenericDialogData function [TAPI 2.2], _tspi_tuispi_providergenericdialogdata, tspi.tuispi_providergenericdialogdata, tspi/TUISPI_providerGenericDialogData
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
 - TUISPI_providerGenericDialogData
 - tspi/TUISPI_providerGenericDialogData
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
 - TUISPI_providerGenericDialogData
---

# TUISPI_providerGenericDialogData function


## -description

The 
<b>TUISPI_providerGenericDialogData</b> function in the UI DLL is called when the service provider sends a 
<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a> message. The service provider uses this to spontaneously update information in dialog boxes created in the application context in conjunction with the processing of particular asynchronous TSPI functions. This function is called from a separate thread from that in which 
<b>TUISPI_providerGenericDialogData</b> is executing. The UI DLL should not block the thread in which this function is called, but should process the data and return immediately (posting a message to the dialog box if necessary).

Implementation is mandatory if 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialog">TUISPI_providerGenericDialog</a> is exported.

## -parameters

### -param htDlgInst

The opaque identifier binding the association of this instance of the function to a particular request from the service provider.

### -param lpParams

Pointer to a memory area used to hold a parameter block. The contents of this parameter block are specific to the service provider and its associated UI DLL. The conveyance of data through this parameter block is one-way to the UI DLL; changes made to the parameter block are not reflected back in the service provider. If this parameter is set to <b>NULL</b>, this is a request to close the dialog box immediately and clean up (
<a href="/windows/desktop/api/tspi/nc-tspi-tuispidllcallback">TUISPIDLLCALLBACK</a> should not be invoked during this cleanup). TAPI invokes this function with <i>lpParams</i> set to <b>NULL</b> to force dialog box cleanup under certain circumstances, such as an application calling 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a> with a dialog box still active.

### -param dwSize

The size in bytes of the parameter block. If the <i>lpParams</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.

## -returns

Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a>



<a href="/windows/desktop/api/tspi/nc-tspi-tuispidllcallback">TUISPIDLLCALLBACK</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>