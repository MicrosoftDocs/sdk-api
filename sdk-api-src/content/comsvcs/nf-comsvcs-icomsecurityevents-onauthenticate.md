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

# IComSecurityEvents::OnAuthenticate


## -description


Generated when a method call level authentication succeeds. When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The identifier of the activity in which the object is created.


### -param ObjectID [in]

The just-in-time activated object.


### -param guidIID [in]

The IID of the method.


### -param iMeth [in]

The v-table index of the method.


### -param cbByteOrig [in]

The number of bytes in the security identifier for the original caller. 


### -param pSidOriginalUser [in]

The security identifier for the original caller.


### -param cbByteCur [in]

The number of bytes in the security identifier for the current caller. 


### -param pSidCurrentUser [in]

The security identifier for the current caller.


### -param bCurrentUserInpersonatingInProc [in]

Indicates whether the current user is impersonating.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/83366f18-8dd4-4c3d-8362-4fbcc4c33b95">IComSecurityEvents</a>
 

 

