---
UID: NC:winsnmp.SNMPAPI_CALLBACK
title: SNMPAPI_CALLBACK (winsnmp.h)
description: The Microsoft WinSNMP implementation calls the SNMPAPI_CALLBACK function to notify a WinSNMP session that an SNMP message or asynchronous event is available.
helpviewer_keywords: ["SNMPAPI_CALLBACK","SNMPAPI_CALLBACK callback","SNMPAPI_CALLBACK callback function [SNMP]","_snmp_snmpapi_callback","snmp.snmpapi_callback","winsnmp/SNMPAPI_CALLBACK"]
old-location: snmp\snmpapi_callback.htm
tech.root: SNMP
ms.assetid: 9871b4a8-c96c-48a7-9e7e-7fe1c259545e
ms.date: 12/05/2018
ms.keywords: SNMPAPI_CALLBACK, SNMPAPI_CALLBACK callback, SNMPAPI_CALLBACK callback function [SNMP], _snmp_snmpapi_callback, snmp.snmpapi_callback, winsnmp/SNMPAPI_CALLBACK
req.header: winsnmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SNMPAPI_CALLBACK
 - winsnmp/SNMPAPI_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winsnmp.h
api_name:
 - SNMPAPI_CALLBACK
---

# SNMPAPI_CALLBACK callback function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft WinSNMP implementation calls the 
<b>SNMPAPI_CALLBACK</b> function to notify a WinSNMP session that an SNMP message or asynchronous event is available.

<b>SNMPAPI_CALLBACK</b> is a placeholder for an application- or library-defined callback function name.

## -parameters

### -param hSession [in]

Handle to the WinSNMP session.

### -param hWnd [in]

Handle to a window of the WinSNMP application to notify when an asynchronous request completes, or when trap notification occurs. This parameter does not have significance for the WinSNMP session, but the implementation always passes the value to the callback function.

### -param wMsg [in]

Specifies an unsigned integer that identifies the notification message to send to the WinSNMP application window. This parameter does not have significance for the WinSNMP session, but the implementation always passes the value to the callback function.

### -param wParam [in]

Specifies an application-defined 32-bit value that identifies the type of notification. If this parameter is equal to zero, an SNMP message is available for the session. The application should call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a> function to retrieve the message. If this parameter is not equal to zero, it indicates an asynchronous event notification for the session. For additional information, see the following Remarks section.

### -param lParam [in]

Specifies an application-defined 32-bit value that specifies the request identifier of the PDU being processed.

### -param lpClientData [in]

If the <i>lpClientData</i> parameter was not <b>NULL</b> on the call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function for this session, this parameter is a pointer to application-defined data.

## -returns

The function must return SNMPAPI_SUCCESS to continue execution of the application. If the function returns any other value, the implementation responds as if the application called the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> function for the indicated session.

## -remarks

When the implementation is executing the retransmission policy for the WinSNMP application and a transmission time-out occurs, the implementation informs the session of the error. In this situation the value of the <i>wParam</i> parameter would be SNMPAPI_TL_TIMEOUT. For a list of other transport layer errors, see the reference pages for the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>, and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a> functions.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>