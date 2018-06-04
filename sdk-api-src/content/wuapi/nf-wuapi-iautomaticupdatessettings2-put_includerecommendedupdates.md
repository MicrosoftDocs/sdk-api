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

# IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates


## -description


<p class="CCE_Message">[<b>Set</b> is no longer supported. Also, starting with 
    Windows 10 calls to <b>Get</b> always return <b>VARIANT_TRUE</b> (include recommended updates). ]


Gets and sets a Boolean value that indicates whether to include optional or recommended updates when a  search for updates and installation of updates is performed.



This property is read/write.


## -parameters


## -remarks



Only administrators can set this property.

The caller can modify the settings in  the <a href="https://msdn.microsoft.com/5ad1a3ee-3293-4825-a85e-ca1e3a38e775">IAutomaticUpdatesSettings2</a> interface only if the <a href="https://msdn.microsoft.com/e7a066b9-9581-4573-82e2-a6f2ca7440ac">ReadOnly</a> property is <b>VARIANT_TRUE</b>.
The <b>ReadOnly</b> property may change after the <a href="https://msdn.microsoft.com/308426d9-d524-406a-931c-1fdb854aa4fb">Refresh</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/5ad1a3ee-3293-4825-a85e-ca1e3a38e775">IAutomaticUpdatesSettings2</a>
 

 

