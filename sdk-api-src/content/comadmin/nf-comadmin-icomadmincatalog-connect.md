---
UID: NF:comadmin.ICOMAdminCatalog.Connect
title: ICOMAdminCatalog::Connect
author: windows-sdk-content
description: Connects to the COM+ catalog on a specified remote computer.
old-location: cos\icomadmincatalog_connect.htm
tech.root: cossdk
ms.assetid: 0fc65ec0-79a7-4544-934d-543f2946c70a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Connect, Connect method [COM+], Connect method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],Connect method, ICOMAdminCatalog.Connect, ICOMAdminCatalog::Connect, _cos_ICOMAdminCatalog_Connect, comadmin/ICOMAdminCatalog::Connect, cos.icomadmincatalog_connect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.Connect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMAdminCatalog::Connect


## -description


Connects to the COM+ catalog on a specified remote computer. 



## -parameters




### -param bstrCatalogServerName [in]

The name of the remote computer. To connect to the local computer, use an empty string.


### -param ppCatalogCollection [out, retval]

The <a href="https://msdn.microsoft.com/en-us/library/ms683140(v=VS.85).aspx">ICatalogCollection</a> interface for the root collection on the remote computer.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <b>Connect</b> method also retrieves a root collection that is bound to the remote computer. A root collection serves as a starting point to locate top-level collections and does not contain any objects or properties.

You can use the <a href="https://msdn.microsoft.com/en-us/library/ms682306(v=VS.85).aspx">GetCollection</a> method to get a top-level collection on the local computer without first using the <b>Connect</b> method.

When you use the <b>Connect</b> method, the <a href="https://msdn.microsoft.com/en-us/library/Ee309561(v=VS.85).aspx">ICOMAdminCatalog</a> interface you are holding works on the computer to which you have connected.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee309561(v=VS.85).aspx">ICOMAdminCatalog</a>
 

 

