---
UID: NF:shobjidl_core.IProfferService.RevokeService
title: IProfferService::RevokeService
author: windows-sdk-content
description: Makes a service unavailable that had previously been available to other objects through IProfferService::ProfferService.
old-location: shell\IProfferService_RevokeService.htm
old-project: shell
ms.assetid: 90868bbb-6fcd-4de1-a853-524542b74701
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IProfferService interface [Windows Shell],RevokeService method, IProfferService.RevokeService, IProfferService::RevokeService, RevokeService, RevokeService method [Windows Shell], RevokeService method [Windows Shell],IProfferService interface, inet_IProfferService_RevokeService, shell.IProfferService_RevokeService, shobjidl_core/IProfferService::RevokeService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IProfferService.RevokeService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IProfferService::RevokeService


## -description


Makes a service unavailable that had previously been available to other objects through <a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">IProfferService::ProfferService</a>.
		


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies an implementation-defined value used for identification purposes. The calling application receives this value from <a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">IProfferService::ProfferService</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91aa5f9a-c276-4822-93e1-9cd2c48ddd9f">IProfferService</a>



<a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">IProfferService::ProfferService</a>
 

 

