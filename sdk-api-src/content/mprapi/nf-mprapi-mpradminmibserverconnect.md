---
UID: NF:mprapi.MprAdminMIBServerConnect
title: MprAdminMIBServerConnect function
author: windows-driver-content
description: The MprAdminMIBServerConnect function establishes a connection to the router being administered. This call should be made before any other calls to the server. The handle returned by this function is used in subsequent MIB calls.
old-location: rras\mpradminmibserverconnect.htm
old-project: RRAS
ms.assetid: 8d8cba34-e5d3-42ae-9724-361802f21410
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MprAdminMIBServerConnect, MprAdminMIBServerConnect function [RAS], _mpr_mpradminmibserverconnect, mprapi/MprAdminMIBServerConnect, rras.mpradminmibserverconnect
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprAdminMIBServerConnect
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminMIBServerConnect function


## -description


The 
<b>MprAdminMIBServerConnect</b> function establishes a connection to the router being administered. This call should be made before any other calls to the server. The handle returned by this function is used in subsequent MIB calls.


## -parameters




### -param lpwsServerName [in]

Pointer to a Unicode string that specifies the name of the remote server. If the caller specifies <b>NULL</b> for this parameter, the function returns a handle to the local server.


### -param phMibServer [out]

Pointer to a handle variable. This variable receives a handle to the server.


## -returns



If the function succeeds, the return value is NO_ERROR.




## -see-also




<a href="https://msdn.microsoft.com/63ea910a-b9d7-43a3-97ae-2f9c26b52059">MprAdminMIBServerDisconnect</a>



<a href="https://msdn.microsoft.com/c911daa4-4f3d-4944-9dc0-695a4efbcb1b">Router Management MIB Functions</a>



<a href="https://msdn.microsoft.com/a7a28ac0-c6f9-450c-9925-67990a62ba08">Router Management MIB Reference</a>
 

 

