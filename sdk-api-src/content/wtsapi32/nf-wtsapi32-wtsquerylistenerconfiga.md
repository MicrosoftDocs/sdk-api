---
UID: NF:wtsapi32.WTSQueryListenerConfigA
title: WTSQueryListenerConfigA function (wtsapi32.h)
description: Retrieves configuration information for a Remote Desktop Services listener.
old-location: termserv\wtsquerylistenerconfig.htm
tech.root: TermServ
ms.assetid: abdcb98e-c00c-444f-a6f9-ce98161c8b62
ms.date: 12/05/2018
ms.keywords: WTSQueryListenerConfig, WTSQueryListenerConfig function [Remote Desktop Services], WTSQueryListenerConfigA, WTSQueryListenerConfigW, termserv.wtsquerylistenerconfig, wtsapi32/WTSQueryListenerConfig, wtsapi32/WTSQueryListenerConfigA, wtsapi32/WTSQueryListenerConfigW
ms.topic: function
f1_keywords:
- wtsapi32/WTSQueryListenerConfig
dev_langs:
- c++
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
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wtsapi32.dll
api_name:
- WTSQueryListenerConfig
- WTSQueryListenerConfigA
- WTSQueryListenerConfigW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WTSQueryListenerConfigA function


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

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wtslistenerconfiga">WTSLISTENERCONFIG</a> structure that receives the  retrieved listener configuration information.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



This function does not retrieve the security descriptor for the listener. To retrieve the security descriptor, call the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya">WTSGetListenerSecurity</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya">WTSGetListenerSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wtslistenerconfiga">WTSLISTENERCONFIG</a>
 

 

