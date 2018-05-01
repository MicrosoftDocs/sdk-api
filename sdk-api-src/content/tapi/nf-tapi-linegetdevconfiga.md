---
UID: NF:tapi.lineGetDevConfigA
title: lineGetDevConfigA function
author: windows-driver-content
description: The lineGetDevConfig function returns an &#0034;opaque&#0034; data structure object, the contents of which are specific to the line (service provider) and device class.
old-location: tapi2\linegetdevconfig.htm
old-project: Tapi
ms.assetid: 39ff5ddb-142e-4f11-9395-e2c3a3ac7d19
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "_tapi2_linegetdevconfig, lineGetDevConfig, lineGetDevConfig function [TAPI 2.2], lineGetDevConfigA, lineGetDevConfigW, tapi/lineGetDevConfig, tapi/lineGetDevConfigA, tapi/lineGetDevConfigW, tapi2.linegetdevconfig"
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
req.unicode-ansi: lineGetDevConfigW (Unicode) and lineGetDevConfigA (ANSI)
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
-	lineGetDevConfig
-	lineGetDevConfigA
-	lineGetDevConfigW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetDevConfigA function


## -description


The 
<b>lineGetDevConfig</b> function returns an "opaque" data structure object, the contents of which are specific to the line (service provider) and device class. The data structure object stores the current configuration of a media-stream device associated with the line device.


## -parameters




### -param dwDeviceID

Identifier of the line device to be configured.


### -param lpDeviceConfig

Pointer to the memory location of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> where the device configuration structure is returned. Upon successful completion of the request, this location is filled with the device configuration. The <b>dwStringFormat</b> member in the 
<b>VARSTRING</b> structure is set to STRINGFORMAT_BINARY. Prior to calling 
<b>lineGetDevConfig</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

### -param lpszDeviceClass

Pointer to a null-terminated string that specifies the device class of the device whose configuration is requested. Valid device class 
<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a> strings are the same as those specified for the function.


## -returns



Returns zero if the function succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NODRIVER, LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_NODEVICE.




## -remarks



Call states are device specific.

The 
<b>lineGetDevConfig</b> function can be used to retrieve a data structure from TAPI that specifies the configuration of a media stream device associated with a particular line device. For example, the contents of this structure could specify data rate, character format, modulation schemes, and error control protocol settings for a "datamodem" media device associated with the line.

Typically, an application calls 
<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a> to identify the media stream device associated with a line, and then calls 
<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a> to allow the user to set up the device configuration. It could then call 
<b>lineGetDevConfig</b>, and save the configuration information in a phone book (or other database) associated with a particular call destination. When the user later wishes to call the same destination again, 
<a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a> can be used to restore the configuration settings selected by the user. The functions 
<b>lineSetDevConfig</b>, 
<b>lineConfigDialog</b>, and 
<b>lineGetDevConfig</b> can be used, in that order, to allow the user to view and update the settings.

The exact format of the data contained within the structure is specific to the line and media stream API (device class), is undocumented, and is undefined. The structure returned by this function cannot be directly accessed or manipulated by the application, but can only be stored intact and later used in 
<a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a> to restore the settings. The structure also cannot necessarily be passed to other devices, even of the same device class (although this can work in some instances, it is not guaranteed).




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>



<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a>



<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>



<a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a>
 

 

