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

# CreateGPOLink function


## -description


The <b>CreateGPOLink</b> function creates a link between 
    the specified GPO and the specified site, domain, or organizational unit.


## -parameters




### -param lpGPO [in]

A value that specifies the path to the GPO, in ADSI format 
      ("LDAP://cn=<i>user</i>, ou=<i>users</i>, dc=<i>coname</i>, dc=<i>com</i>"). 
      You cannot specify a server name in this parameter.


### -param lpContainer [in]

A value that specifies the Active Directory path to the site, domain, or organizational unit.


### -param fHighPriority [in]

A value that specifies the link priority. If this parameter is <b>TRUE</b>, the system 
      creates the link as the highest priority. If this parameter is <b>FALSE</b>, the system 
      creates the link as the lowest priority.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns 
       one of the COM error codes defined in the header file WinError.h. Be aware that you should test explicitly for 
       the return value <b>S_OK</b>. Do not use the <b>SUCCEEDED</b> or 
       <b>FAILED</b> macro on the returned <b>HRESULT</b> to determine success or failure of the 
       function.




## -see-also




<a href="https://msdn.microsoft.com/164b1d10-9ec0-43c8-80fe-be1ad8ec991f">DeleteAllGPOLinks</a>



<a href="https://msdn.microsoft.com/e797bc8d-c0c5-4d93-b553-6c07029af01f">DeleteGPOLink</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

