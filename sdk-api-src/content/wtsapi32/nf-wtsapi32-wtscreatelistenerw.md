---
UID: NF:wtsapi32.WTSCreateListenerW
title: WTSCreateListenerW function (wtsapi32.h)
description: Creates a new Remote Desktop Services listener or configures an existing listener. (Unicode)
helpviewer_keywords: ["WTSCreateListener", "WTSCreateListener function [Remote Desktop Services]", "WTSCreateListenerW", "WTS_LISTENER_CREATE", "WTS_LISTENER_UPDATE", "termserv.wtscreatelistener", "wtsapi32/WTSCreateListener", "wtsapi32/WTSCreateListenerW"]
old-location: termserv\wtscreatelistener.htm
tech.root: TermServ
ms.assetid: 057facde-43b6-44c4-944a-7ad7854ec1e6
ms.date: 12/05/2018
ms.keywords: WTSCreateListener, WTSCreateListener function [Remote Desktop Services], WTSCreateListenerA, WTSCreateListenerW, WTS_LISTENER_CREATE, WTS_LISTENER_UPDATE, termserv.wtscreatelistener, wtsapi32/WTSCreateListener, wtsapi32/WTSCreateListenerA, wtsapi32/WTSCreateListenerW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSCreateListenerW (Unicode) and WTSCreateListenerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSCreateListenerW
 - wtsapi32/WTSCreateListenerW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSCreateListener
 - WTSCreateListenerA
 - WTSCreateListenerW
---

# WTSCreateListenerW function


## -description

Creates a new Remote Desktop Services listener or configures an existing listener.

## -parameters

### -param hServer [in]

A handle to an RD Session Host server. Always set this  parameter to <b>WTS_CURRENT_SERVER_HANDLE</b>.

### -param pReserved [in]

This parameter is reserved. Always set this parameter to <b>NULL</b>.

### -param Reserved [in]

This parameter is reserved. Always set this parameter to zero.

### -param pListenerName [in]

A pointer to a null-terminated string that contains the name of the listener to create or configure.

### -param pBuffer [in]

A pointer to a <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtslistenerconfiga">WTSLISTENERCONFIG</a> structure that contains configuration information for the listener.

### -param flag [in]

The purpose of the call. This parameter can be one of the following values.



#### WTS_LISTENER_CREATE (1 (0x1))

Create a new listener.



#### WTS_LISTENER_UPDATE (16 (0x10))

Update the settings of an existing listener.


##### - flag.WTS_LISTENER_CREATE (1 (0x1))

Create a new listener.


##### - flag.WTS_LISTENER_UPDATE (16 (0x10))

Update the settings of an existing listener.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

This function creates or configures a listener that uses   <a href="/windows/desktop/TermServ/remote-desktop-protocol">Remote Desktop Protocol</a> (RDP). Always set the <b>version</b> member of the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtslistenerconfiga">WTSLISTENERCONFIG</a> structure that is pointed to by the <i>pBuffer</i> parameter to one.

This function does not create or configure the security descriptor of the listener. When you call this function to create a new listener, the function assigns the default security descriptor to the new listener. To modify the security descriptor, call the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetlistenersecuritya">WTSSetListenerSecurity</a> function. For more information about security descriptors, see  <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>.

This function does not validate the settings for the new listener. Be sure that the settings are valid before calling this function.





> [!NOTE]
> The wtsapi32.h header defines WTSCreateListener as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtslistenerconfiga">WTSLISTENERCONFIG</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetlistenersecuritya">WTSSetListenerSecurity</a>
