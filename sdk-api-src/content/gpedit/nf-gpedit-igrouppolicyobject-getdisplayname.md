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

# IGroupPolicyObject::GetDisplayName


## -description


The
    <b>GetDisplayName</b> method retrieves the display name for the GPO.


## -parameters




### -param pszName [out]

Pointer to a buffer that receives the display name.


### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To set the display name for a GPO, you can call the 
<a href="https://msdn.microsoft.com/979e8399-83e1-421e-8f32-813464ac97aa">SetDisplayName</a> method. Call 
<a href="https://msdn.microsoft.com/1374c01c-aba3-48f5-8a42-7139873d8f7c">GetName</a> to retrieve the unique name for a GPO, which is a GUID for an Active Directory object.




## -see-also




<a href="https://msdn.microsoft.com/1374c01c-aba3-48f5-8a42-7139873d8f7c">GetName</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>



<a href="https://msdn.microsoft.com/979e8399-83e1-421e-8f32-813464ac97aa">SetDisplayName</a>
 

 

