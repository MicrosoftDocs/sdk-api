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

# IGPEInformation::GetHint


## -description


The
    <b>GetHint</b> method retrieves the type of Active Directory object to which this GPO can be linked.


## -parameters




### -param gpHint [out]

Receives the directory service type. This parameter can be one of the following values.



#### GPHintUnknown

No link information is available.



#### GPHintMachine

The object can be linked to a computer (local or remote).



#### GPHintSite

The object can be linked to a site.



#### GPHintDomain

The object can be linked to a domain.



#### GPHintOrganizationalUnit

The object can be linked to an organizational unit.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



The Group Policy Object Editor cannot determine which Active Directory objects are linked to a particular GPO. The 
<b>GetHint</b> method provides linking information based on how the user started the Group Policy Object Editor. It can be started in the following ways:

<ul>
<li>As an extension to the Active Directory Manager. Navigate to the site, domain, or organizational unit, then select <a href="https://msdn.microsoft.com/0e9314f4-bdea-47b1-81a4-9b19b79ac49d">Group Policy</a>.</li>
<li>As a stand-alone MMC tool with a specific link.</li>
<li>As a stand-alone MMC tool without a specific link.</li>
</ul>
You may want to customize your application's user interface based on the result of calling this method. However, use this method with caution because the returned value may indicate the wrong scope.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a>
 

 

