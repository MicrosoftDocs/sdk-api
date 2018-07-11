---
UID: NS:mprapi._PPP_NBFCP_INFO
title: "_PPP_NBFCP_INFO"
author: windows-sdk-content
description: The PPP_NBFCP_INFO structure contains the result of a PPP NetBEUI Framer (NBF) projection operation.
old-location: rras\ppp_nbfcp_info.htm
old-project: rras
ms.assetid: 376c662d-c0e1-4136-937c-47a4681c14ec
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: PPP_NBFCP_INFO, PPP_NBFCP_INFO structure [RAS], _PPP_NBFCP_INFO, _mpr_ppp_nbfcp_info, mprapi/PPP_NBFCP_INFO, rras.ppp_nbfcp_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PPP_NBFCP_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_NBFCP_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _PPP_NBFCP_INFO structure


## -description


The 
<b>PPP_NBFCP_INFO</b> structure contains the result of a PPP NetBEUI Framer (NBF) projection operation.


## -struct-fields




### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.


### -field wszWksta

Specifies a Unicode string that is the local workstation's computer name. This unique computer name is the closest NetBIOS equivalent to a client's NetBEUI address on a remote access connection.


## -remarks



The 
<b>PPP_NBFCP_INFO</b> structure can be used only when administrating computers that are running an operating system prior to Windows Server 2003 as later operating systems do not support the NetBEUI protocol.




## -see-also




<a href="https://msdn.microsoft.com/39692a38-ab40-43da-a704-8c206be72ceb">PPP_INFO</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

