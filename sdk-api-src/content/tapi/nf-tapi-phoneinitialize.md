---
UID: NF:tapi.phoneInitialize
title: phoneInitialize function
author: windows-sdk-content
description: The phoneInitialize function is obsolete. It continues to be exported by Tapi.dll and Tapi32.dll for backward compatibility with applications using TAPI versions 1.3 and 1.4.
old-location: tapi2\phoneinitialize.htm
old-project: Tapi
ms.assetid: e06153c1-707e-45a9-8d26-747d53e16cf2
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_phoneinitialize, phoneInitialize, phoneInitialize function [TAPI 2.2], tapi/phoneInitialize, tapi2.phoneinitialize"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	phoneInitialize
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneInitialize function


## -description


The 
<b>phoneInitialize</b> function is obsolete. It continues to be exported by Tapi.dll and Tapi32.dll for backward compatibility with applications using TAPI versions 1.3 and 1.4.

Applications using TAPI version 2.0 or later must use 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a> instead.

<b>For TAPI Versions 1.4 and Earlier:  </b>The 
<b>phoneInitialize</b> function initializes the application's use of TAPI for the subsequent use of the phone functions in the Telephony API. It registers the application's specified notification mechanism and returns the number of phone devices that are available to the application.


## -parameters




### -param lphPhoneApp

Pointer to a location that is filled with the application's usage handle for TAPI.


### -param hInstance

Instance handle of the client application or DLL.


### -param lpfnCallback

Address of a callback function that is invoked to determine status and events on the phone device.


### -param lpszAppName

Pointer to a <b>null</b>-terminated string that contains displayable characters. If this parameter is non-<b>NULL</b>, it contains an application-supplied name of the application. This name is provided in the 
<a href="https://msdn.microsoft.com/798a6c57-d3d3-4924-a925-059de350d18e">PHONESTATUS</a> structure to indicate, in a user-friendly way, which application is the current owner of the phone device. This information can be useful for logging and status reporting purposes. If <i>lpszAppName</i> is <b>NULL</b>, the application's filename is used instead.


### -param lpdwNumDevs

Pointer to <b>DWORD</b>. This location is loaded with the number of phone devices available to the application.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPNAME, PHONEERR_INIFILECORRUPT, PHONEERR_INVALPOINTER, PHONEERR_NOMEM, PHONEERR_OPERATIONFAILED, PHONEERR_REINIT, PHONEERR_RESOURCEUNAVAIL, PHONEERR_NODEVICE, PHONEERR_NODRIVER, PHONEERR_INVALPARAM




## -remarks



The application can refer to individual phone devices by using phone device identifiers that range from zero to <i>dwNumDevs</i> minus one. An application should not assume that these phone devices are capable of anything beyond what is specified by the Assisted Telephony subset without first querying their device capabilities with the 
<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a> function.

Applications should not invoke 
<b>phoneInitialize</b> without subsequently opening a phone (at least for monitoring). If the application is not monitoring and not using any devices, it should call 
<a href="https://msdn.microsoft.com/0cf8bc07-946a-450d-8062-b9e19c22a4c5">phoneShutdown</a> so that memory resources allocated by TAPI can be released if unneeded, and TAPI itself can be unloaded from memory while not needed.

Another reason for performing a 
<b>phoneShutdown</b> is that if a user changes the device configuration (adds or removes a line or phone), there is no way for TAPI to notify an application that has a line or phone handle open at the time. After a reconfiguration has taken place, causing a PHONESTATE_REINIT message to be sent, no applications can open a device until all applications have performed a 
<b>phoneShutdown</b>.

If any service provider fails to initialize properly, the 
<b>phoneInitialize</b> function fails and returns the error indicated by the service provider. If the PHONEERR_INVALPARAM error value is returned, the specified <i>hInstance</i> parameter is invalid.




## -see-also




<a href="https://msdn.microsoft.com/798a6c57-d3d3-4924-a925-059de350d18e">PHONESTATUS</a>



<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>



<a href="https://msdn.microsoft.com/0cf8bc07-946a-450d-8062-b9e19c22a4c5">phoneShutdown</a>
 

 

