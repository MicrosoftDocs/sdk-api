---
UID: NF:mprapi.MprAdminMIBServerDisconnect
title: MprAdminMIBServerDisconnect function
author: windows-sdk-content
description: The MprAdminMIBServerDisconnect function disconnects the connection made by a previous call to MprAdminMIBServerConnect.
old-location: rras\mpradminmibserverdisconnect.htm
old-project: rras
ms.assetid: 63ea910a-b9d7-43a3-97ae-2f9c26b52059
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: MprAdminMIBServerDisconnect, MprAdminMIBServerDisconnect function [RAS], _mpr_mpradminmibserverdisconnect, mprapi/MprAdminMIBServerDisconnect, rras.mpradminmibserverdisconnect
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
 - MprAdminMIBServerDisconnect
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminMIBServerDisconnect function


## -description


The 
<b>MprAdminMIBServerDisconnect</b> function disconnects the connection made by a previous call to 
<a href="https://msdn.microsoft.com/8d8cba34-e5d3-42ae-9724-361802f21410">MprAdminMIBServerConnect</a>.


## -parameters




### -param hMibServer [in]

Handle to the router from which to disconnect. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/8d8cba34-e5d3-42ae-9724-361802f21410">MprAdminMIBServerConnect</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/8d8cba34-e5d3-42ae-9724-361802f21410">MprAdminMIBServerConnect</a>



<a href="https://msdn.microsoft.com/c911daa4-4f3d-4944-9dc0-695a4efbcb1b">Router Management MIB Functions</a>



<a href="https://msdn.microsoft.com/a7a28ac0-c6f9-450c-9925-67990a62ba08">Router Management MIB Reference</a>
 

 

