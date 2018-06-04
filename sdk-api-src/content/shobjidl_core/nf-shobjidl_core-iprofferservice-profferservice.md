---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IProfferService::ProfferService


## -description


Makes a service available to other objects on the same host.


## -parameters




### -param guidService




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
 

 

