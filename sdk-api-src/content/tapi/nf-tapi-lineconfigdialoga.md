---
UID: NF:tapi.lineConfigDialogA
title: lineConfigDialogA function (tapi.h)
description: The lineConfigDialog function causes the provider of the specified line device to display a dialog box (attached to hwndOwner of the application) to allow the user to configure parameters related to the line device. (lineConfigDialogA)
helpviewer_keywords: ["lineConfigDialogA", "tapi/lineConfigDialogA"]
old-location: tapi2\lineconfigdialog.htm
tech.root: tapi3
ms.assetid: 52f23647-e9f5-48a3-95f4-1ac52898cb5a
ms.date: 12/05/2018
ms.keywords: _tapi2_lineconfigdialog, lineConfigDialog, lineConfigDialog function [TAPI 2.2], lineConfigDialogA, lineConfigDialogW, tapi/lineConfigDialog, tapi/lineConfigDialogA, tapi/lineConfigDialogW, tapi2.lineconfigdialog
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineConfigDialogW (Unicode) and lineConfigDialogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineConfigDialogA
 - tapi/lineConfigDialogA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineConfigDialog
 - lineConfigDialogA
 - lineConfigDialogW
---

# lineConfigDialogA function


## -description

The 
<b>lineConfigDialog</b> function causes the provider of the specified line device to display a dialog box (attached to <i>hwndOwner</i> of the application) to allow the user to configure parameters related to the line device.

## -parameters

### -param dwDeviceID

Identifier of the line device to be configured.

### -param hwndOwner

Handle to a window to which the dialog box is to be attached. Can be <b>NULL</b> to indicate that any window created during the function should have no owner window.

### -param lpszDeviceClass

Pointer to a <b>null</b>-terminated string that identifies a device class name. This device class allows the application to select a specific subscreen of configuration information applicable to that device class. This parameter is optional and can be left <b>NULL</b> or empty, in which case the highest level configuration is selected.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NOMEM, LINEERR_INUSE, LINEERR_OPERATIONFAILED, LINEERR_INVALDEVICECLASS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPARAM, LINEERR_UNINITIALIZED, LINEERR_INVALPOINTER, LINEERR_OPERATIONUNAVAIL, LINEERR_NODEVICE.

## -remarks

The 
<b>lineConfigDialog</b> function causes the service provider to display a modal dialog box (attached to <i>hwndOwner</i> of the application) to allow the user to configure parameters related to the line specified by <i>dwDeviceID</i>. The <i>lpszDeviceClass</i> parameter allows the application to select a specific subscreen of configuration information applicable to the device class in which the user is interested; the permitted strings are the same as for 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>. For example, if the line supports the Comm API, passing "COMM" as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, start at the corresponding point in a multilevel configuration dialog box chain, so the user doesn't have to "dig" to find the parameters of interest).

The <i>lpszDeviceClass</i> parameter would be "tapi/line" , "", or <b>NULL</b> to cause the provider to display the highest level configuration for the line.





> [!NOTE]
> The tapi.h header defines lineConfigDialog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>
