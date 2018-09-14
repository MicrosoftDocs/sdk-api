---
UID: NF:tspi.TSPI_lineConfigDialogEdit
title: TSPI_lineConfigDialogEdit function
author: windows-sdk-content
description: The TSPI_lineConfigDialogEdit function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_lineConfigDialogEdit.
old-location: tspi\tspi_lineconfigdialogedit.htm
tech.root: TAPI
ms.assetid: 7248050c-0e59-406a-b75c-d06c0ce7bdc5
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TSPI_lineConfigDialogEdit, TSPI_lineConfigDialogEdit function [TAPI 2.2], _tspi_tspi_lineconfigdialogedit, tspi.tspi_lineconfigdialogedit, tspi/TSPI_lineConfigDialogEdit
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
 - TSPI_lineConfigDialogEdit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineConfigDialogEdit function


## -description


The 
<b>TSPI_lineConfigDialogEdit</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="https://msdn.microsoft.com/05169974-31f3-445b-b55f-5931bace6505">TUISPI_lineConfigDialogEdit</a>.

The 
<b>TSPI_lineConfigDialogEdit</b> function causes the provider of the specified line device to display a modal dialog box as a child window of <i>hwndOwner</i> to allow the user to configure parameters related to the line device.


## -parameters




### -param dwDeviceID

The line device to be configured.


### -param hwndOwner

A handle to a window to which the dialog box is to be attached.


### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated Unicode string that identifies a device class name. This device class allows the caller to select a specific subscreen of configuration information applicable to that device class. If this parameter is <b>NULL</b> or points to an empty string, the highest level configuration is selected. The permitted strings are the same as for 
<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>.


### -param lpDeviceConfigIn

A pointer to the opaque configuration data structure that was returned by 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a> (or a previous invocation of 
<b>TSPI_lineConfigDialogEdit</b>) in the variable portion of the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure.


### -param dwSize

The number of bytes in the structure pointed to by <i>lpDeviceConfigIn</i>. This value is returned in the <b>dwStringSize</b> member in the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure returned by 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a> or a previous invocation of 
<b>TSPI_lineConfigDialogEdit</b>.


### -param lpDeviceConfigOut

A pointer to the memory location of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> where the device configuration structure is returned. Upon successful completion of the request, this location is filled with the device configuration. The <b>dwStringFormat</b> member in the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure is set to STRINGFORMAT_BINARY. Prior to calling 
<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a> (or a future invocation of 
<a href="https://msdn.microsoft.com/417016c3-8053-4a70-bce4-b96cce5e09a5">lineConfigDialogEdit</a>), the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the request succeeds or an error number if an error occurs. Possible return values are:

LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONFAILED, LINEERR_INVALPARAM, LINEERR_RESOURCEUNAVAIL, LINEERR_NODRIVER, LINEERR_OPERATIONUNAVAIL, LINEERR_NOMEM.




## -remarks



This function causes the service provider to display a modal dialog box (attached to <i>hwndOwner</i>) to allow the user to configure parameters related to the line specified by <i>dwDeviceID</i>.

The <i>lpszDeviceClass</i> parameter selects a specific subscreen of configuration information applicable to the device class in which the user is interested; the permitted strings are the same as for 
<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>. For example, if the line supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, start at the corresponding point in a multilevel configuration dialog box chain, so the user doesn't have to "dig" to find the parameters of interest).

The <i>lpszDeviceClass</i> parameter is "tapi/line", "", or <b>NULL</b> to cause the provider to display the highest level configuration for the line.

The difference between this function and 
<a href="https://msdn.microsoft.com/b0f26029-ddb2-472c-8a09-2abf213dab16">TSPI_lineConfigDialog</a> is the source of the parameters to edit and the result of the editing. In 
<b>TSPI_lineConfigDialog</b>, the parameters edited are those currently in use on the device (or set for use on the next call), and any changes made have (to the maximum extent possible) an immediate impact on any active connection; also, the application must use 
<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a> to fetch the result of parameter changes from 
<b>TSPI_lineConfigDialog</b>. With 
<b>TSPI_lineConfigDialogEdit</b>, the parameters to edit are passed in from the application, and the results are returned to the application, with no impact on active connections; the results of the editing are returned with this function, and the application does not need to call 
<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a>. Thus, 
<b>TSPI_lineConfigDialogEdit</b> permits an application to provide the ability for the user to set up parameters for future calls without having an impact on any active call. However, the output of this function can be passed to 
<a href="https://msdn.microsoft.com/41699ca8-a30d-48ab-bace-bc2b95b67e77">TSPI_lineSetDevConfig</a> to affect the current call or next call.

For backward compatibility, this function is not exported by older service providers. TAPI detects this condition and reports LINEERR_OPERATIONUNAVAIL if an application attempts to call this function on an older provider.




## -see-also




<a href="https://msdn.microsoft.com/b0f26029-ddb2-472c-8a09-2abf213dab16">TSPI_lineConfigDialog</a>



<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a>



<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>



<a href="https://msdn.microsoft.com/41699ca8-a30d-48ab-bace-bc2b95b67e77">TSPI_lineSetDevConfig</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>
 

 

