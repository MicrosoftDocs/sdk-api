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

# IAssociatedIdentityProvider::AssociateIdentity


## -description


The <b>AssociateIdentity</b> method associates an identity with a local user account.


## -parameters




### -param hwndParent [in]

A handle to the parent of the window used to collect account credentials.


### -param ppPropertyStore [out]

A pointer to the <b>IPropertyStore</b> interface associated with the identity.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method should call <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> to collect account credentials.




## -see-also




<a href="https://msdn.microsoft.com/007d5daf-f0cf-4bfb-bd87-bb949bf90126">IAssociatedIdentityProvider</a>
 

 

