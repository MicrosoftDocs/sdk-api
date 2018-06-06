---
UID: NF:wtsapi32.WTSCreateListenerW
title: WTSCreateListenerW function
author: windows-sdk-content
description: Creates a new Remote Desktop Services listener or configures an existing listener.
old-location: termserv\wtscreatelistener.htm
old-project: TermServ
ms.assetid: 057facde-43b6-44c4-944a-7ad7854ec1e6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: WTSCreateListener, WTSCreateListener function [Remote Desktop Services], WTSCreateListenerA, WTSCreateListenerW, WTS_LISTENER_CREATE, WTS_LISTENER_UPDATE, termserv.wtscreatelistener, wtsapi32/WTSCreateListener, wtsapi32/WTSCreateListenerA, wtsapi32/WTSCreateListenerW
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
req.unicode-ansi: WTSCreateListenerW (Unicode) and WTSCreateListenerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
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
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

A pointer to a <a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a> structure that contains configuration information for the listener.


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
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



This function creates or configures a listener that uses   <a href="https://msdn.microsoft.com/442c3c7f-d04b-4dcd-945d-f6e0168c59d5">Remote Desktop Protocol</a> (RDP). Always set the <b>version</b> member of the <a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a> structure that is pointed to by the <i>pBuffer</i> parameter to one.

This function does not create or configure the security descriptor of the listener. When you call this function to create a new listener, the function assigns the default security descriptor to the new listener. To modify the security descriptor, call the <a href="https://msdn.microsoft.com/bc90d526-e252-4506-b781-66da5bd66ced">WTSSetListenerSecurity</a> function. For more information about security descriptors, see  <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>.

This function does not validate the settings for the new listener. Be sure that the settings are valid before calling this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a>



<a href="https://msdn.microsoft.com/bc90d526-e252-4506-b781-66da5bd66ced">WTSSetListenerSecurity</a>
 

 

