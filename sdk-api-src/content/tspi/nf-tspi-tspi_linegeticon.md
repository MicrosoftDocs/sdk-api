---
UID: NF:tspi.TSPI_lineGetIcon
title: TSPI_lineGetIcon function
author: windows-sdk-content
description: The TSPI_lineGetIcon function retrieves a service line device-specific icon to display to the user.
old-location: tspi\tspi_linegeticon.htm
tech.root: Tapi
ms.assetid: 0fa8a030-1b56-4d14-affd-ba1574696a3c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TSPI_lineGetIcon, TSPI_lineGetIcon function [TAPI 2.2], _tspi_tspi_linegeticon, tspi.tspi_linegeticon, tspi/TSPI_lineGetIcon
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
 - TSPI_lineGetIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineGetIcon function


## -description


The 
<b>TSPI_lineGetIcon</b> function retrieves a service line device-specific icon to display to the user.


## -parameters




### -param dwDeviceID

The line device whose icon is requested.


### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated Unicode string that identifies a device class name. This device class allows the caller to select an icon specific to that device class. This parameter is optional and can be left <b>NULL</b>, in which case the highest level icon associated with the line device rather than a specified media stream device is selected. 




Permitted strings are the same as for 
<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>. For example, if the line supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to return an icon related specifically to the Comm device functions of the service provider.


### -param lphIcon

A pointer to a memory location in which the handle to the icon is returned.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_OPERATIONUNAVAIL.




## -remarks



The provider should return a handle (in the <b>DWORD</b> pointed to by <i>lphIcon</i>) to an icon resource (obtained from the  
<a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a> function) associated with the specified line.

A provider may choose to support many icons (selected by <i>lpszDeviceClass</i> and/or line number), a single icon (such as for the manufacturer, which would be returned for all 
<b>TSPI_lineGetIcon</b> requests regardless of the <i>lpszDeviceClass</i> selected), or no icons, in which case it sets the <b>DWORD</b> pointed to by <i>lphIcon</i> to <b>NULL</b>. TAPI examines the handle returned by the provider, and if the provider returns <b>NULL</b>, TAPI substitutes a generic  Telephony icon (the generic "line" icon).




## -see-also




<a href="https://msdn.microsoft.com/b0f26029-ddb2-472c-8a09-2abf213dab16">TSPI_lineConfigDialog</a>



<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>
 

 

