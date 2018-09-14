---
UID: NF:tapi.lineConfigDialogA
title: lineConfigDialogA function
author: windows-sdk-content
description: The lineConfigDialog function causes the provider of the specified line device to display a dialog box (attached to hwndOwner of the application) to allow the user to configure parameters related to the line device.
old-location: tapi2\lineconfigdialog.htm
tech.root: TAPI
ms.assetid: 52f23647-e9f5-48a3-95f4-1ac52898cb5a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "_tapi2_lineconfigdialog, lineConfigDialog, lineConfigDialog function [TAPI 2.2], lineConfigDialogA, lineConfigDialogW, tapi/lineConfigDialog, tapi/lineConfigDialogA, tapi/lineConfigDialogW, tapi2.lineconfigdialog"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>. For example, if the line supports the Comm API, passing "COMM" as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, start at the corresponding point in a multilevel configuration dialog box chain, so the user doesn't have to "dig" to find the parameters of interest).

The <i>lpszDeviceClass</i> parameter would be "tapi/line" , "", or <b>NULL</b> to cause the provider to display the highest level configuration for the line.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>
 

 

