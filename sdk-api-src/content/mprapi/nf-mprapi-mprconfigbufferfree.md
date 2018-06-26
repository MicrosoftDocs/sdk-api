---
UID: NF:mprapi.MprConfigBufferFree
title: MprConfigBufferFree function
author: windows-sdk-content
description: The MprConfigBufferFree function frees buffers allocated by calls to the following functions:
old-location: rras\mprconfigbufferfree.htm
old-project: RRAS
ms.assetid: d7df56ee-72e4-4b0c-87a3-a1f66d791b62
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: MprConfigBufferFree, MprConfigBufferFree function [RAS], _mpr_mprconfigbufferfree, mprapi/MprConfigBufferFree, rras.mprconfigbufferfree
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
 - MprConfigBufferFree
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigBufferFree function


## -description


The 
<b>MprConfigBufferFree</b> function frees buffers allocated by calls to the following functions:

MprConfigXEnum
			

MprConfigXGetInfo
			

where X stands for Server, 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn895657">Interface</a>, Transport, or InterfaceTransport.


## -parameters




### -param pBuffer [in]

Pointer to a memory buffer allocated by a previous call to: 




MprConfigXEnum
						

MprConfigXGetInfo
						

where X stands for Server, 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn895657">Interface</a>, Transport, or InterfaceTransport.


## -returns



If the function succeeds, the return value is NO_ERROR.




## -see-also




<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>



<a href="https://msdn.microsoft.com/f33f9e66-1668-4839-9c98-5945104110bc">MprConfigInterfaceGetInfo</a>



<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>



<a href="https://msdn.microsoft.com/2b0bb412-a480-43ff-b29a-cf4e7674d2c4">MprConfigInterfaceTransportGetInfo</a>



<a href="https://msdn.microsoft.com/6d3cd97a-96ef-4ecd-b2fd-2743ba79aa5b">MprConfigServerGetInfo</a>



<a href="https://msdn.microsoft.com/2abe30f4-564b-499f-a6d3-13da305a783c">MprConfigTransportEnum</a>



<a href="https://msdn.microsoft.com/84054313-f923-47d6-8019-c68a042d2d73">MprConfigTransportGetInfo</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

