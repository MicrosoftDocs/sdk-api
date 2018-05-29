---
UID: NF:mprapi.MprAdminAcceptNewLink
title: MprAdminAcceptNewLink function
author: windows-sdk-content
description: Remote Access Service (RAS) calls the MprAdminAcceptNewLink function each time a link is created for a particular connection.
old-location: rras\mpradminacceptnewlink.htm
old-project: RRAS
ms.assetid: a4cbca7d-a8b0-4396-9201-648bcca6a8c8
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: MprAdminAcceptNewLink, MprAdminAcceptNewLink callback, MprAdminAcceptNewLink callback function [RAS], _mpr_mpradminacceptnewlink, mprapi/MprAdminAcceptNewLink, rras.mpradminacceptnewlink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mprapi.h
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Mprapi.h
api_name:
-	MprAdminAcceptNewLink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminAcceptNewLink function


## -description


Remote Access Service (RAS) calls the 
<b>MprAdminAcceptNewLink</b> function each time a link is created for a particular connection. RAS calls this function once immediately after 
<a href="https://msdn.microsoft.com/6ca7fe28-53e1-49e0-ab3c-4e8e4343c88c">MprAdminAcceptNewConnection</a> returns, and an additional time for every new link that is to be used with the connection.


## -parameters




### -param pRasPort0 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/361b065e-8240-465f-a0fe-d4bfc097ec70">RAS_PORT_0</a> structure that describes the port being used by the link.


### -param pRasPort1 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/4850f08e-13ee-485f-99a5-be4554d6311b">RAS_PORT_1</a> structure that describes the port being used by the link.


## -returns



If RAS should accept the new link, the return value should be <b>TRUE</b>.

If RAS should not accept the new link, the return value should be <b>FALSE</b>.




## -remarks



RAS supports multiple Administration DLLs. RAS calls the multiple implementations of 
<b>MprAdminAcceptNewLink</b> in the order in which the DLLs are listed in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926940">registry</a>. The remote-access user is allowed to connect only if the implementation of 
<b>MprAdminAcceptNewLink</b> in each of the DLLs accepts the connection. In other words, every DLL must accept the link in order for the link to be established.

<b>Windows 2000 Server and earlier:  </b>If RAS does not accept the new link, RAS does not call the 
<a href="https://msdn.microsoft.com/7f2b30e8-ba1d-4db3-843f-f9eafca47add">MprAdminLinkHangupNotification</a> function.

Do not call any of the 
<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a> or 
<a href="https://msdn.microsoft.com/e58fa4a6-16d3-4953-bf21-887d08e25af7">RAS User Administration Functions</a> from inside 
<b>MprAdminAcceptNewLink</b>. Calls to these functions do not return when made from within a callout function.




## -see-also




<a href="https://msdn.microsoft.com/6ca7fe28-53e1-49e0-ab3c-4e8e4343c88c">MprAdminAcceptNewConnection</a>



<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a>



<a href="https://msdn.microsoft.com/7f2b30e8-ba1d-4db3-843f-f9eafca47add">MprAdminLinkHangupNotification</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/361b065e-8240-465f-a0fe-d4bfc097ec70">RAS_PORT_0</a>



<a href="https://msdn.microsoft.com/4850f08e-13ee-485f-99a5-be4554d6311b">RAS_PORT_1</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

