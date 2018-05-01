---
UID: NF:tapi.lineConfigDialogEditW
title: lineConfigDialogEditW function
author: windows-driver-content
description: The lineConfigDialogEdit function causes the provider of the specified line device to display a dialog box (attached to hwndOwner of the application) to allow the user to configure parameters related to the line device.
old-location: tapi2\lineconfigdialogedit.htm
old-project: Tapi
ms.assetid: 417016c3-8053-4a70-bce4-b96cce5e09a5
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "_tapi2_lineconfigdialogedit, lineConfigDialogEdit, lineConfigDialogEdit function [TAPI 2.2], lineConfigDialogEditA, lineConfigDialogEditW, tapi/lineConfigDialogEdit, tapi/lineConfigDialogEditA, tapi/lineConfigDialogEditW, tapi2.lineconfigdialogedit"
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
req.unicode-ansi: lineConfigDialogEditW (Unicode) and lineConfigDialogEditA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineConfigDialogEdit
-	lineConfigDialogEditA
-	lineConfigDialogEditW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineConfigDialogEditW function


## -description


The 
<b>lineConfigDialogEdit</b> function causes the provider of the specified line device to display a dialog box (attached to <i>hwndOwner</i> of the application) to allow the user to configure parameters related to the line device.


## -parameters




### -param dwDeviceID

Identifier of the line device to be configured.


### -param hwndOwner

Handle to a window to which the dialog box is to be attached. Can be <b>NULL</b> to indicate that any window created during the function should have no owner window.


### -param lpszDeviceClass

Pointer to a <b>null</b>-terminated string that identifies a device class name. This device class allows the application to select a specific subscreen of configuration information applicable to that device class. This parameter is optional and can be left <b>NULL</b> or empty, in which case the highest level configuration is selected.


### -param lpDeviceConfigIn

Pointer to the opaque configuration data structure that was returned by 
<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a> (or a previous invocation of 
<b>lineConfigDialogEdit</b>) in the variable portion of the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure.


### -param dwSize

Number of bytes in the structure pointed to by <i>lpDeviceConfigIn</i>. This value is returned in the <b>dwStringSize</b> member in the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure returned by 
<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a> or a previous invocation of 
<b>lineConfigDialogEdit</b>. 


### -param lpDeviceConfigOut

Pointer to the memory location of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> where the device configuration structure is returned. Upon successful completion of the request, this location is filled with the device configuration. The <b>dwStringFormat</b> member in the 
<b>VARSTRING</b> structure is set to STRINGFORMAT_BINARY. Prior to calling 
<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a> (or a future invocation of 
<b>lineConfigDialogEdit</b>), the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_OPERATIONFAILED, LINEERR_INVALDEVICECLASS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPARAM, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NODRIVER, LINEERR_OPERATIONUNAVAIL, LINEERR_NOMEM, LINEERR_NODEVICE.




## -remarks



If LINEERR_STRUCTURETOOSMALL is returned, the <b>dwTotalSize</b> member of the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure pointed to by <i>lpDeviceConfigOut</i> does not specify enough memory to contain the entire configuration structure. The <b>dwNeededSize</b> member has been set to the amount required. To the extent that user entries were reflected in information that could not be returned due to insufficient space, those edits are lost; applications should therefore allocate the maximum amount of space that may be needed by the device class to return its configuration structure (for more information, see 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">TAPI Device Classes</a>).

The 
<b>lineConfigDialogEdit</b> function causes the service provider to display a modal dialog box (attached to <i>hwndOwner</i> of the application) to allow the user to configure parameters related to the line specified by <i>dwDeviceID</i>.

The <i>lpszDeviceClass</i> parameter allows the application to select a specific subscreen of configuration information applicable to the device class in which the user is interested; the permitted strings are the same as for 
<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>. For example, if the line supports the Comm API, passing "COMM" as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, start at the corresponding point in a multilevel configuration dialog box chain, so the user doesn't have to "dig" to find the parameters of interest).

The <i>lpszDeviceClass</i> parameter would be "tapi/line" , "", or <b>NULL</b> to cause the provider to display the highest level configuration for the line.

The difference between this function and 
<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a> is the source of the parameters to edit and the result of the editing. In 
<b>lineConfigDialog</b>, the parameters edited are those currently in use on the device (or set for use on the next call), and any changes made have (to the maximum extent possible) an immediate impact on any active connection; also, the application must use 
<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a> to fetch the result of parameter changes from 
<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a>. With 
<b>lineConfigDialogEdit</b>, the parameters to edit are passed in from the application, and the results are returned to the application, with no impact on active connections; the results of the editing are returned with this function, and the application does not need to call 
<b>lineGetDevConfig</b>. Thus, 
<b>lineConfigDialogEdit</b> permits an application to provide the ability for the user to set up parameters for future calls without having an impact on any active call. However, the output of this function can be passed to 
<a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a> to affect the current call or next call.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>



<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a>



<a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a>



<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>



<a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a>
 

 

