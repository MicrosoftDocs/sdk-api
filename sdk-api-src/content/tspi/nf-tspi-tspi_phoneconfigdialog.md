---
UID: NF:tspi.TSPI_phoneConfigDialog
title: TSPI_phoneConfigDialog function (tspi.h)
description: The TSPI_phoneConfigDialog function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_phoneConfigDialog.
helpviewer_keywords: ["TSPI_phoneConfigDialog","TSPI_phoneConfigDialog function [TAPI 2.2]","_tspi_tspi_phoneconfigdialog","tspi.tspi_phoneconfigdialog","tspi/TSPI_phoneConfigDialog"]
old-location: tspi\tspi_phoneconfigdialog.htm
tech.root: tapi3
ms.assetid: cce9460c-0914-4f02-a6a4-efb7f43ed22a
ms.date: 12/05/2018
ms.keywords: TSPI_phoneConfigDialog, TSPI_phoneConfigDialog function [TAPI 2.2], _tspi_tspi_phoneconfigdialog, tspi.tspi_phoneconfigdialog, tspi/TSPI_phoneConfigDialog
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
 - TSPI_phoneConfigDialog
 - tspi/TSPI_phoneConfigDialog
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
 - TSPI_phoneConfigDialog
---

# TSPI_phoneConfigDialog function


## -description

The 
<b>TSPI_phoneConfigDialog</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_phoneconfigdialog">TUISPI_phoneConfigDialog</a>.

The 
<b>TSPI_phoneConfigDialog</b> function causes the provider of the specified phone device to display a modal dialog box as a child window of <i>hwndOwner</i> to allow the user to configure parameters related to the phone device.

## -parameters

### -param dwDeviceID

The phone device to be configured.

### -param hwndOwner

A handle to a parent window in which the dialog box window is to be placed.

### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated Unicode string that identifies a device class name. This device class allows the caller to select a specific subscreen of configuration information applicable to that device class. If this parameter is <b>NULL</b> or an empty string, the highest level configuration dialog box is selected.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_BADDEVICEID, PHONEERR_NOMEM, PHONEERR_INUSE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPARAM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INVALDEVICECLASS, PHONEERR_RESOURCEUNAVAIL.

## -remarks

<b>TSPI_phoneConfigDialog</b> causes the service provider to display a modal dialog box as a child window of <i>hWndOwner</i> to allow the user to configure parameters related to the phone specified by <i>dwDeviceID</i>. The <i>lpszDeviceClass</i> parameter allows the application to select a specific subscreen of configuration information applicable to the device class in which the user is interested. The permitted strings are the same as for 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetid">TSPI_phoneGetID</a>. For example, if the phone supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, to start at the corresponding point in a multilevel configuration dialog box chain, so that the user doesn't have to search to find the desired parameters). The <i>szDeviceClass</i> parameter should be "tapi/phone", "", or <b>NULL</b> to cause the provider to display the highest level configuration for the phone.

The procedure must update the [Windows Telephony] section in the Win.ini file and broadcast the WM_WININICHANGE message if it makes any changes to Telephon.ini that affect the contents of structures visible to applications (such as 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>), or if phone devices are created or removed.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetid">TSPI_phoneGetID</a>