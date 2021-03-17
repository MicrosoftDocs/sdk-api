---
UID: NF:tspi.TUISPI_lineConfigDialogEdit
title: TUISPI_lineConfigDialogEdit function (tspi.h)
description: The TUISPI_lineConfigDialogEdit function causes the provider of the specified line device to display a modal dialog box as a child window of hwndOwner to allow the user to configure parameters related to the line device.
helpviewer_keywords: ["TUISPI_lineConfigDialogEdit","TUISPI_lineConfigDialogEdit function [TAPI 2.2]","_tspi_tuispi_lineconfigdialogedit","tspi.tuispi_lineconfigdialogedit","tspi/TUISPI_lineConfigDialogEdit"]
old-location: tspi\tuispi_lineconfigdialogedit.htm
tech.root: tapi3
ms.assetid: 05169974-31f3-445b-b55f-5931bace6505
ms.date: 12/05/2018
ms.keywords: TUISPI_lineConfigDialogEdit, TUISPI_lineConfigDialogEdit function [TAPI 2.2], _tspi_tuispi_lineconfigdialogedit, tspi.tuispi_lineconfigdialogedit, tspi/TUISPI_lineConfigDialogEdit
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
 - TUISPI_lineConfigDialogEdit
 - tspi/TUISPI_lineConfigDialogEdit
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
 - TUISPI_lineConfigDialogEdit
---

# TUISPI_lineConfigDialogEdit function


## -description

The 
<b>TUISPI_lineConfigDialogEdit</b> function causes the provider of the specified line device to display a modal dialog box as a child window of <i>hwndOwner</i> to allow the user to configure parameters related to the line device. This function makes the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconfigdialogedit">TSPI_lineConfigDialogEdit</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

Implementation is optional.

## -parameters

### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box.

### -param dwDeviceID

The line device to be configured.

### -param hwndOwner

A handle to a window to which the dialog box is to be attached.

### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated Unicode string that identifies a device class name. This device class allows the caller to select a specific subscreen of configuration information applicable to that device class. If this parameter is <b>NULL</b> or points to an empty string, the highest level configuration is selected. The permitted strings are the same as for 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>.

### -param lpDeviceConfigIn

A pointer to the opaque configuration data structure that was returned by 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevconfig">TSPI_lineGetDevConfig</a> (or a previous invocation of 
<b>TUISPI_lineConfigDialogEdit</b>) in the variable portion of the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure.

### -param dwSize

The number of bytes in the structure pointed to by <i>lpDeviceConfigIn</i>. This value is returned in the <b>dwStringSize</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure returned by 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevconfig">TSPI_lineGetDevConfig</a> or a previous invocation of 
<b>TUISPI_lineConfigDialogEdit</b>. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

### -param lpDeviceConfigOut

A pointer to the memory location of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> where the device configuration structure is returned. Upon successful completion of the request, this location is filled with the device configuration. The <b>dwStringFormat</b> member in the 
<b>VARSTRING</b> structure is set to STRINGFORMAT_BINARY. Prior to calling 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a> (or a future invocation of 
<a href="/windows/desktop/api/tapi/nf-tapi-lineconfigdialogedit">lineConfigDialogEdit</a>), the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns zero if the request succeeds or an error number if an error occurs. Possible return values are:

LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONFAILED, LINEERR_INVALPARAM, LINEERR_RESOURCEUNAVAIL, LINEERR_NODRIVER, LINEERR_OPERATIONUNAVAIL, LINEERR_NOMEM.

## -remarks

The <i>lpszDeviceClass</i> parameter selects a specific subscreen of configuration information applicable to the device class in which the user is interested; the permitted strings are the same as for 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>. For example, if the line supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, start at the corresponding point in a multilevel configuration dialog box chain, so the user doesn't have to "dig" to find the parameters of interest).

The <i>lpszDeviceClass</i> parameter is "tapi/line", "", or <b>NULL</b> to cause the provider to display the highest level configuration for the line.

The difference between this function and 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialog">TUISPI_lineConfigDialog</a> is the source of the parameters to edit and the result of the editing. In 
<b>TUISPI_lineConfigDialog</b>, the parameters edited are those currently in use on the device (or set for use on the next call), and any changes made have (to the maximum extent possible) an immediate impact on any active connection; also, the application must use 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a> to fetch the result of parameter changes from 
<b>TUISPI_lineConfigDialog</b>. With 
<b>TUISPI_lineConfigDialogEdit</b>, the parameters to edit are passed in from the application, and the results are returned to the application, with no impact on active connections; the results of the editing are returned with this function, and the application does not need to call 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>. Thus, 
<b>TUISPI_lineConfigDialogEdit</b> permits an application to provide the ability for the user to set up parameters for future calls without having an impact on any active call. However, the output of this function can be passed to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a> to affect the current call or next call.

For backward compatibility, this function is not exported by older service providers. TAPI detects this condition and reports LINEERR_OPERATIONUNAVAIL if an application attempts to call this function on an older provider.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevconfig">TSPI_lineGetDevConfig</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialog">TUISPI_lineConfigDialog</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>