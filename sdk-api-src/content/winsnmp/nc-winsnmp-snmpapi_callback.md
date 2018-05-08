---
UID: NC:winsnmp.SNMPAPI_CALLBACK
title: SNMPAPI_CALLBACK
author: windows-driver-content
description: The Microsoft WinSNMP implementation calls the SNMPAPI_CALLBACK function to notify a WinSNMP session that an SNMP message or asynchronous event is available.
old-location: snmp\snmpapi_callback.htm
old-project: SNMP
ms.assetid: 9871b4a8-c96c-48a7-9e7e-7fe1c259545e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SNMPAPI_CALLBACK, SNMPAPI_CALLBACK callback, SNMPAPI_CALLBACK callback function [SNMP], _snmp_snmpapi_callback, snmp.snmpapi_callback, winsnmp/SNMPAPI_CALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winsnmp.h
api_name:
-	SNMPAPI_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SNMPAPI_CALLBACK callback function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

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
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> function to retrieve the message. If this parameter is not equal to zero, it indicates an asynchronous event notification for the session. For additional information, see the following Remarks section.


### -param lParam [in]

Specifies an application-defined 32-bit value that specifies the request identifier of the PDU being processed.


### -param lpClientData [in]

If the <i>lpClientData</i> parameter was not <b>NULL</b> on the call to the 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a> function for this session, this parameter is a pointer to application-defined data.


## -returns



The function must return SNMPAPI_SUCCESS to continue execution of the application. If the function returns any other value, the implementation responds as if the application called the 
<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a> function for the indicated session.




## -remarks



When the implementation is executing the retransmission policy for the WinSNMP application and a transmission time-out occurs, the implementation informs the session of the error. In this situation the value of the <i>wParam</i> parameter would be SNMPAPI_TL_TIMEOUT. For a list of other transport layer errors, see the reference pages for the 
<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a>, 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>, and 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a>



<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

