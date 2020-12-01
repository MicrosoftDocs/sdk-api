---
UID: NF:tspi.TUISPI_lineConfigDialog
title: TUISPI_lineConfigDialog function (tspi.h)
description: The TUISPI_lineConfigDialog function causes the provider of the specified line device to display a modal dialog box as a child window of hwndOwner to allow the user to configure parameters related to the line device.
helpviewer_keywords: ["TUISPI_lineConfigDialog","TUISPI_lineConfigDialog function [TAPI 2.2]","_tspi_tuispi_lineconfigdialog","tspi.tuispi_lineconfigdialog","tspi/TUISPI_lineConfigDialog"]
old-location: tspi\tuispi_lineconfigdialog.htm
tech.root: tapi3
ms.assetid: 405af7aa-eb0b-49a1-9712-2f86357fc720
ms.date: 12/05/2018
ms.keywords: TUISPI_lineConfigDialog, TUISPI_lineConfigDialog function [TAPI 2.2], _tspi_tuispi_lineconfigdialog, tspi.tuispi_lineconfigdialog, tspi/TUISPI_lineConfigDialog
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
 - TUISPI_lineConfigDialog
 - tspi/TUISPI_lineConfigDialog
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
 - TUISPI_lineConfigDialog
---

# TUISPI_lineConfigDialog function


## -description

The 
<b>TUISPI_lineConfigDialog</b> function causes the provider of the specified line device to display a modal dialog box as a child window of <i>hwndOwner</i> to allow the user to configure parameters related to the line device. This function makes the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconfigdialog">TSPI_lineConfigDialog</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

Implementation is optional.

## -parameters

### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box and to send updated configuration to the service provider.

### -param dwDeviceID

The line device to be configured.

### -param hwndOwner

A handle to a parent window in which the dialog box window is to be placed.

### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated string that identifies a device class name. This device class allows the caller to select a specific subscreen of configuration information applicable to that device class. If this parameter is <b>NULL</b> or an empty string, the highest level configuration dialog box should be selected. The permitted strings are the same as for 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>. For example, if the line supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, to start at the corresponding point in a multilevel configuration dialog box chain, so that the user doesn't have to search to find the desired parameters.)

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INUSE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

There is no restriction that 
<b>TUISPI_lineConfigDialog</b> be called only when the line is closed. However, each provider can impose such a restriction itself. When 
<b>TUISPI_lineConfigDialog</b> is called, the provider could alert the user with the message "The line is in use by one or more applications. You may not change the line configuration while the line is in use" (and return the error message LINEERR_INUSE). However, some configurations may be safe to change "on the fly," particularly those related to media types (such as the modem error control protocol), especially when that media type is not currently in use. The provider could allow those options to be changed while the line is open.

Users should not be allowed to change anything that alters values returned with 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> or 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> without first forcibly closing the line as a signal that applications must call functions that return these structures in order to have accurate information.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevconfig">TSPI_lineGetDevConfig</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a>