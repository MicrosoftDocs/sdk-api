---
UID: NF:mprapi.MprAdminConnectionHangupNotificationEx
title: MprAdminConnectionHangupNotificationEx function
author: windows-driver-content
description: Remote Access Service (RAS) calls the MprAdminConnectionHangupNotificationEx function after the last link for the specified connection has been dismantled.
old-location: rras\mpradminconnectionhangupnotificationex.htm
old-project: RRAS
ms.assetid: de251e1b-53ff-45c8-8e2e-65ac26b4a7f5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MprAdminConnectionHangupNotificationEx, MprAdminConnectionHangupNotificationEx callback, MprAdminConnectionHangupNotificationEx callback function [RAS], mprapi/MprAdminConnectionHangupNotificationEx, rras.mpradminconnectionhangupnotificationex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Mprapi.h
api_name:
-	MprAdminConnectionHangupNotificationEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminConnectionHangupNotificationEx function


## -description


Remote Access Service (RAS) calls the 
<b>MprAdminConnectionHangupNotificationEx</b> function after the last link for the specified connection has been dismantled.


## -parameters




### -param pRasConn [in]

A pointer to a 
<a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure that describes this connection.


## -returns



This function does not have a return value.




## -see-also




<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a>



<a href="https://msdn.microsoft.com/3231ae83-c7fc-46d4-a4d9-f7ccf1c4ed18">MprAdminConnectionHangupNotification2</a>



<a href="https://msdn.microsoft.com/8c31d345-8f57-47f5-a021-e399f7ccca5d">MprAdminConnectionHangupNotification3</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

