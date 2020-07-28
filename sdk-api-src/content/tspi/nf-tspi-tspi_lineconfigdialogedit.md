---
UID: NF:tspi.TSPI_lineConfigDialogEdit
title: TSPI_lineConfigDialogEdit function (tspi.h)
description: The TSPI_lineConfigDialogEdit function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_lineConfigDialogEdit.
helpviewer_keywords: ["TSPI_lineConfigDialogEdit","TSPI_lineConfigDialogEdit function [TAPI 2.2]","_tspi_tspi_lineconfigdialogedit","tspi.tspi_lineconfigdialogedit","tspi/TSPI_lineConfigDialogEdit"]
old-location: tspi\tspi_lineconfigdialogedit.htm
tech.root: tapi3
ms.assetid: 7248050c-0e59-406a-b75c-d06c0ce7bdc5
ms.date: 12/05/2018
ms.keywords: TSPI_lineConfigDialogEdit, TSPI_lineConfigDialogEdit function [TAPI 2.2], _tspi_tspi_lineconfigdialogedit, tspi.tspi_lineconfigdialogedit, tspi/TSPI_lineConfigDialogEdit
f1_keywords:
- tspi/TSPI_lineConfigDialogEdit
dev_langs:
- c++
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
- TSPI_lineConfigDialogEdit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_lineConfigDialogEdit function


## -description


The 
<b>TSPI_lineConfigDialogEdit</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialogedit">TUISPI_lineConfigDialogEdit</a>.

The 
<b>TSPI_lineConfigDialogEdit</b> function causes the provider of the specified line device to display a modal dialog box as a child window of <i>hwndOwner</i> to allow the user to configure parameters related to the line device.


## -parameters




### -param dwDeviceID

The line device to be configured.


### -param hwndOwner

A handle to a window to which the dialog box is to be attached.


### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated Unicode string that identifies a device class name. This device class allows the caller to select a specific subscreen of configuration information applicable to that device class. If this parameter is <b>NULL</b> or points to an empty string, the highest level configuration is selected. The permitted strings are the same as for 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>.


### -param lpDeviceConfigIn

A pointer to the opaque configuration data structure that was returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevconfig">TSPI_lineGetDevConfig</a> (or a previous invocation of 
<b>TSPI_lineConfigDialogEdit</b>) in the variable portion of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure.


### -param dwSize

The number of bytes in the structure pointed to by <i>lpDeviceConfigIn</i>. This value is returned in the <b>dwStringSize</b> member in the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevconfig">TSPI_lineGetDevConfig</a> or a previous invocation of 
<b>TSPI_lineConfigDialogEdit</b>.


### -param lpDeviceConfigOut

A pointer to the memory location of type 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> where the device configuration structure is returned. Upon successful completion of the request, this location is filled with the device configuration. The <b>dwStringFormat</b> member in the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure is set to STRINGFORMAT_BINARY. Prior to calling 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a> (or a future invocation of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineconfigdialogedit">lineConfigDialogEdit</a>), the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the request succeeds or an error number if an error occurs. Possible return values are:

LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONFAILED, LINEERR_INVALPARAM, LINEERR_RESOURCEUNAVAIL, LINEERR_NODRIVER, LINEERR_OPERATIONUNAVAIL, LINEERR_NOMEM.




## -remarks



This function causes the service provider to display a modal dialog box (attached to <i>hwndOwner</i>) to allow the user to configure parameters related to the line specified by <i>dwDeviceID</i>.

The <i>lpszDeviceClass</i> parameter selects a specific subscreen of configuration information applicable to the device class in which the user is interested; the permitted strings are the same as for 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>. For example, if the line supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, start at the corresponding point in a multilevel configuration dialog box chain, so the user doesn't have to "dig" to find the parameters of interest).

The <i>lpszDeviceClass</i> parameter is "tapi/line", "", or <b>NULL</b> to cause the provider to display the highest level configuration for the line.

The difference between this function and 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_lineconfigdialog">TSPI_lineConfigDialog</a> is the source of the parameters to edit and the result of the editing. In 
<b>TSPI_lineConfigDialog</b>, the parameters edited are those currently in use on the device (or set for use on the next call), and any changes made have (to the maximum extent possible) an immediate impact on any active connection; also, the application must use 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a> to fetch the result of parameter changes from 
<b>TSPI_lineConfigDialog</b>. With 
<b>TSPI_lineConfigDialogEdit</b>, the parameters to edit are passed in from the application, and the results are returned to the application, with no impact on active connections; the results of the editing are returned with this function, and the application does not need to call 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>. Thus, 
<b>TSPI_lineConfigDialogEdit</b> permits an application to provide the ability for the user to set up parameters for future calls without having an impact on any active call. However, the output of this function can be passed to 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a> to affect the current call or next call.

For backward compatibility, this function is not exported by older service providers. TAPI detects this condition and reports LINEERR_OPERATIONUNAVAIL if an application attempts to call this function on an older provider.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_lineconfigdialog">TSPI_lineConfigDialog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevconfig">TSPI_lineGetDevConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>
 

 

