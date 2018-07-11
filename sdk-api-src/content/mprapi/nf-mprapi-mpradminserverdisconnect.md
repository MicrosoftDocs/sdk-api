---
UID: NF:mprapi.MprAdminServerDisconnect
title: MprAdminServerDisconnect function
author: windows-sdk-content
description: The MprAdminServerDisconnect function disconnects the connection made by a previous call to MprAdminServerConnect.
old-location: rras\mpradminserverdisconnect.htm
old-project: rras
ms.assetid: 905b5296-ae6b-40a6-ba49-837db96de152
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: MprAdminServerDisconnect, MprAdminServerDisconnect function [RAS], _mpr_mpradminserverdisconnect, mprapi/MprAdminServerDisconnect, rras.mpradminserverdisconnect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminServerDisconnect
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminServerDisconnect function


## -description


The 
<b>MprAdminServerDisconnect</b> function disconnects the connection made by a previous call to 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


## -parameters




### -param hMprServer [in]

Handle to the router from which to disconnect. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

