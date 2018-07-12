---
UID: NF:tspi.TUISPI_phoneConfigDialog
title: TUISPI_phoneConfigDialog function
author: windows-sdk-content
description: The TUISPI_phoneConfigDialog function causes the provider of the specified phone device to display a modal dialog box as a child window of hwndOwner to allow the user to configure parameters related to the phone device.
old-location: tspi\tuispi_phoneconfigdialog.htm
old-project: tapi
ms.assetid: 6bdd4206-0028-43f0-8da8-2fc11779f7d2
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: TUISPI_phoneConfigDialog, TUISPI_phoneConfigDialog function [TAPI 2.2], _tspi_tuispi_phoneconfigdialog, tspi.tuispi_phoneconfigdialog, tspi/TUISPI_phoneConfigDialog
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TUISPI_phoneConfigDialog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TUISPI_phoneConfigDialog function


## -description


The 
<b>TUISPI_phoneConfigDialog</b> function causes the provider of the specified phone device to display a modal dialog box as a child window of <i>hwndOwner</i> to allow the user to configure parameters related to the phone device. This function makes the 
<a href="https://msdn.microsoft.com/cce9460c-0914-4f02-a6a4-efb7f43ed22a">TSPI_phoneConfigDialog</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

Implementation is optional.


## -parameters




### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box and to send updated configuration to the service provider.


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



The <i>lpszDeviceClass</i> parameter allows the application to select a specific subscreen of configuration information applicable to the device class in which the user is interested. The permitted strings are the same as for 
<a href="https://msdn.microsoft.com/ed34641d-091a-45a3-becc-b5fca36a9367">TSPI_phoneGetID</a>.

For example, if the phone supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, to start at the corresponding point in a multilevel configuration dialog box chain, so that the user doesn't have to search to find the desired parameters). The <i>szDeviceClass</i> parameter should be "tapi/phone", "", or <b>NULL</b> to cause the provider to display the highest level configuration for the phone.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/ed34641d-091a-45a3-becc-b5fca36a9367">TSPI_phoneGetID</a>
 

 

