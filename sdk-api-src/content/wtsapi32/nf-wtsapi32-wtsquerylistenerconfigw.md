---
UID: NF:wtsapi32.WTSQueryListenerConfigW
title: WTSQueryListenerConfigW function
author: windows-sdk-content
description: Retrieves configuration information for a Remote Desktop Services listener.
old-location: termserv\wtsquerylistenerconfig.htm
old-project: TermServ
ms.assetid: abdcb98e-c00c-444f-a6f9-ce98161c8b62
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: WTSQueryListenerConfig, WTSQueryListenerConfig function [Remote Desktop Services], WTSQueryListenerConfigA, WTSQueryListenerConfigW, termserv.wtsquerylistenerconfig, wtsapi32/WTSQueryListenerConfig, wtsapi32/WTSQueryListenerConfigA, wtsapi32/WTSQueryListenerConfigW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSQueryListenerConfigW (Unicode) and WTSQueryListenerConfigA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wtsapi32.dll
api_name:
-	WTSQueryListenerConfig
-	WTSQueryListenerConfigA
-	WTSQueryListenerConfigW
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSQueryListenerConfigW function


## -description


Retrieves configuration information for a Remote Desktop Services listener.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Always set this  parameter to <b>WTS_CURRENT_SERVER_HANDLE</b>.


### -param pReserved [in]

This parameter is reserved. Always set this parameter to <b>NULL</b>.


### -param Reserved [in]

This parameter is reserved. Always set this parameter to zero.


### -param pListenerName [in]

A pointer to a null-terminated string that contains the name of the listener to query.


### -param pBuffer [out]

A pointer to a <a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a> structure that receives the  retrieved listener configuration information.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



This function does not retrieve the security descriptor for the listener. To retrieve the security descriptor, call the <a href="https://msdn.microsoft.com/6e49df9a-679d-4cc1-9297-90cf1e3509fa">WTSGetListenerSecurity</a> function.




## -see-also




<a href="https://msdn.microsoft.com/6e49df9a-679d-4cc1-9297-90cf1e3509fa">WTSGetListenerSecurity</a>



<a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a>
 

 

