---
UID: NF:shobjidl_core.IProfferService.ProfferService
title: IProfferService::ProfferService
author: windows-sdk-content
description: Makes a service available to other objects on the same host.
old-location: shell\IProfferService_ProfferService.htm
tech.root: shell
ms.assetid: ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IProfferService interface [Windows Shell],ProfferService method, IProfferService.ProfferService, IProfferService::ProfferService, ProfferService, ProfferService method [Windows Shell], ProfferService method [Windows Shell],IProfferService interface, inet_IProfferService_ProfferService, shell.IProfferService_ProfferService, shobjidl_core/IProfferService::ProfferService
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IProfferService.ProfferService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProfferService::ProfferService


## -description


Makes a service available to other objects on the same host.


## -parameters




### -param guidService

TBD


### -param psp [in]

Type: <b><a href="_inet_IServiceProvider_Interface">IServiceProvider</a>*</b>

A pointer to an <a href="_inet_IServiceProvider_Interface">IServiceProvider</a> interface.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> that receives an implementation-defined value used for identification purposes. The calling application must keep track of this value for possible use in <a href="https://msdn.microsoft.com/90868bbb-6fcd-4de1-a853-524542b74701">IProfferService::RevokeService</a>.


#### - rguidService [in]

Type: <b>REFGUID</b>

A value of type <b>GUID</b> that specifies the service being offered.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91aa5f9a-c276-4822-93e1-9cd2c48ddd9f">IProfferService</a>



<a href="https://msdn.microsoft.com/90868bbb-6fcd-4de1-a853-524542b74701">IProfferService::RevokeService</a>



<a href="_inet_IServiceProvider_Interface">IServiceProvider</a>
 

 

