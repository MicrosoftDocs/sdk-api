---
UID: NF:ntdsapi.DsBindToISTGA
title: DsBindToISTGA function
author: windows-sdk-content
description: Binds to the computer that holds the Inter-Site Topology Generator (ISTG) role in the domain of the local computer.
old-location: ad\dsbindtoistg.htm
old-project: AD
ms.assetid: bd53124c-8578-495d-b540-d4b4c09297c3
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DsBindToISTG, DsBindToISTG function [Active Directory], DsBindToISTGA, DsBindToISTGW, ad.dsbindtoistg, ntdsapi/DsBindToISTG, ntdsapi/DsBindToISTGA, ntdsapi/DsBindToISTGW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBindToISTGW (Unicode) and DsBindToISTGA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsBindToISTG
 - DsBindToISTGA
 - DsBindToISTGW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: ADAM
---

# DsBindToISTGA function


## -description


The <b>DsBindToISTG</b> function binds to the computer that holds the Inter-Site Topology Generator (ISTG) role in the domain of the local computer.


## -parameters




### -param SiteName [in, optional]

Pointer to a null-terminated string that contains the site name used when binding. If this parameter is <b>NULL</b>, the site of the nearest domain controller is used.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the bind handle. To close this handle, call <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a>.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error code otherwise.
       The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a>
 

 

