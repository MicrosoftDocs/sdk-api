---
UID: NF:clfsmgmtw32.DeregisterManageableLogClient
title: DeregisterManageableLogClient function
author: windows-sdk-content
description: Deregisters a client with the log manager.
old-location: fs\deregistermanageablelogclient.htm
old-project: Clfs
ms.assetid: 293a4856-62d4-49a3-9177-4d09a0897200
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: DeregisterManageableLogClient, DeregisterManageableLogClient function [Files], clfsmgmtw32/DeregisterManageableLogClient, fs.deregistermanageablelogclient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clfsmgmtw32.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: CLFS_MGMT_POLICY, *PCLFS_MGMT_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - DeregisterManageableLogClient
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# DeregisterManageableLogClient function


## -description


The <b>DeregisterManageableLogClient</b> function deregisters a client with the log manager.


## -parameters




### -param hLog [in]

The handle to deregister.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/ca7969a1-e391-4e3f-96a8-5fb23c400d7e">RegisterManageableLogClient</a>
 

 

