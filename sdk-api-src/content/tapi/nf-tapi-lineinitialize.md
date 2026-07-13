---
UID: NF:tapi.lineInitialize
title: lineInitialize function (tapi.h)
description: The lineInitialize function is obsolete. It continues to be exported by Tapi.dll and Tapi32.dll for backward compatibility with applications using API versions 1.3 and 1.4.
helpviewer_keywords: ["_tapi2_lineinitialize","lineInitialize","lineInitialize function [TAPI 2.2]","tapi/lineInitialize","tapi2.lineinitialize"]
old-location: tapi2\lineinitialize.htm
tech.root: tapi3
ms.assetid: 4b406f19-be9b-4130-91a7-5fdfa56f7fc3
ms.date: 12/05/2018
ms.keywords: _tapi2_lineinitialize, lineInitialize, lineInitialize function [TAPI 2.2], tapi/lineInitialize, tapi2.lineinitialize
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineInitialize
 - tapi/lineInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
 - Ext-MS-Win-ras-tapi32-l1-1-0.dll
api_name:
 - lineInitialize
---

# lineInitialize function


## -description

The 
<b>lineInitialize</b> function is obsolete. It continues to be exported by Tapi.dll and Tapi32.dll for backward compatibility with applications using API versions 1.3 and 1.4.

Applications using API version 2.0 or later must use 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a> instead.

<b>For TAPI Versions  1.4 and Earlier:  </b> The 
<b>lineInitialize</b> function initializes the application's use of Tapi.dll for subsequent use of the line abstraction. The function registers the application's specified notification mechanism and returns the number of line devices available to the application. A line device is any device that provides an implementation for the line-prefixed functions in TAPI.

## -parameters

### -param lphLineApp

Pointer to a location that is filled with the application's usage handle for TAPI.

### -param hInstance

Instance handle of the client application or DLL.

### -param lpfnCallback

Address of a callback function that is invoked to determine status and events on the line device, addresses, or calls. For more information, see 
<a href="/windows/desktop/api/tapi/nc-tapi-linecallback">lineCallbackFunc</a>.

### -param lpszAppName

Pointer to a <b>null</b>-terminated text string that contains only displayable characters. If this parameter is not <b>NULL</b>, it contains an application-supplied name for the application. This name is provided in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure to indicate, in a user-friendly way, which application originated, or originally accepted or answered the call. This information can be useful for call logging purposes. If <i>lpszAppName</i> is <b>NULL</b>, the application's file name is used instead.

### -param lpdwNumDevs

Pointer to a <b>DWORD</b>-sized location. Upon successful completion of this request, this location is filled with the number of line devices available to the application.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPNAME, LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_REINIT, LINEERR_NODRIVER, LINEERR_NODEVICE, LINEERR_NOMEM, LINEERR_NOMULTIPLEINSTANCE.

## -remarks

If LINEERR_REINIT is returned and TAPI reinitialization has been requested (for example as a result of adding or removing a telephony service provider), then 
<b>lineInitialize</b> requests are rejected with this error until the last application shuts down its usage of the API (using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>). At that time, the new configuration becomes effective and applications are once again permitted to call 
<b>lineInitialize</b>. If the LINEERR_INVALPARAM error value is returned, the specified <i>hInstance</i> parameter is invalid.

The application can refer to individual line devices by using line device identifiers that range from zero to <i>dwNumDevs</i> minus one. An application should not assume that these line devices are capable of anything beyond what is specified by the Basic Telephony subset without first querying their device capabilities using 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a> and 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>.

Applications should not invoke 
<b>lineInitialize</b> without subsequently opening a line (at least for monitoring). If the application is not monitoring and not using any devices, it should call 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a> so that memory resources allocated by Tapi.dll can be released if unneeded, and Tapi.dll itself can be unloaded from memory while not needed.

Another reason for performing a 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a> is that if a user changes the device configuration (adds or removes a line or phone), there is no way for TAPI to notify an application that has a line or phone handle open at the time. After a reconfiguration has taken place, causing a LINEDEVSTATE_REINIT message to be sent, no applications can open a device until all applications have performed a 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>. If any service provider fails to initialize properly, this function fails and returns the error indicated by the service provider.

On all TAPI platforms, 
<b>lineInitialize</b> is equivalent to 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a> using the LINEINITIALIZEEXOPTION_USEHIDDENWINDOW option.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/api/tapi/nc-tapi-linecallback">lineCallbackFunc</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>