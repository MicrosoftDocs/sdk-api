---
UID: NF:tspi.TSPI_lineGetID
title: TSPI_lineGetID function
author: windows-sdk-content
description: The TSPI_lineGetID function returns a device identifier for the specified device class associated with the selected line, address, or call.
old-location: tspi\tspi_linegetid.htm
old-project: tapi
ms.assetid: d4331721-61c3-4de0-bb1f-c27f475170d1
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_lineGetID, TSPI_lineGetID function [TAPI 2.2], _tspi_tspi_linegetid, tspi.tspi_linegetid, tspi/TSPI_lineGetID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tspi.h
req.include-header: 
req.redist: 
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
 - TSPI_lineGetID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineGetID function


## -description


The 
<b>TSPI_lineGetID</b> function returns a device identifier for the specified device class associated with the selected line, address, or call.


## -parameters




### -param hdLine

The service provider's handle to the line to be queried.


### -param dwAddressID

An address on the given open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades. TAPI does not validate this parameter when this function is called.


### -param hdCall

The service provider's handle to the call to be queried.


### -param dwSelect

Specifies whether the device identifier requested is associated with the line, address, or a single call. The <i>dwSelect</i> parameter can have only one of the 
<a href="https://msdn.microsoft.com/f19a41bc-403a-4d4b-ab85-240a73514ebb">LINECALLSELECT_ constants</a>.


### -param lpDeviceID

A pointer to the memory location of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> where the device identifier is returned. Upon successful completion of the request, this location is filled with the device identifier. The format of the returned information depends on the method used by the device class (API) for naming devices.


### -param lpszDeviceClass

A pointer to a null-terminated Unicode string that specifies the device class of the device whose identifier is requested. Valid device class strings are those used in the System.ini section to identify device classes (such as COM, Wave, and MCI.)


### -param hTargetProcess

The process handle of the application on behalf of which the 
<b>TSPI_lineGetID</b> function is invoked. If the information returned in the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure includes a handle for use by the application, the service provider should create or duplicate the handle for the process. 




If <i>hTargetProcess</i> is set to INVALID_HANDLE_VALUE, then the application is executing on a remote client system and it is not possible to create a duplicate handle directly. Instead, the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure should contain a UNC name of a network device or other name that the remote client can use to access the device. If this is not possible, then the function should fail.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NODEVICE, LINEERR_RESOURCEUNAVAIL.




## -remarks



The service provide returns LINEERR_INVALLINEHANDLE if <i>dwSelect</i> is LINECALLSELECT_LINE or LINECALLSELECT_ADDRESS, and <i>hdLine</i> is invalid.

The service provider returns LINEERR_INVALCALLHANDLE if <i>dwSelect</i> is LINECALLSELECT_CALL and <i>hdCall</i> is invalid.

The service provider should support the tapi/line device class to allow applications to determine the real line device identifier of an opened line. In that case, the variable data returned is the <i>dwDeviceID</i>. For more information about common device class names, see 
<a href="https://msdn.microsoft.com/b29ea789-d017-4e35-b77a-c0d54ac54c66">TSPI Device Classes</a>.

A vendor that defines a device-specific media type also needs to define the corresponding device-specific (proprietary) API to manage devices of the media type. To avoid collisions on device class names assigned independently by different vendors, a vendor should select a name that uniquely identifies the vendor and then the media type; for example: "intel/video".

The service provider fills in all the members of the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

The service provider does not need to be concerned with handling tapi/line and tapi/phone device classes because TAPI handles these for the service provider. Therefore, code for handling these device classes is optional.




## -see-also




<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a>



<a href="https://msdn.microsoft.com/41699ca8-a30d-48ab-bace-bc2b95b67e77">TSPI_lineSetDevConfig</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>
 

 

