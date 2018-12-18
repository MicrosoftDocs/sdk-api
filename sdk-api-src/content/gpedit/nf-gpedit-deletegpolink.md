---
UID: NF:gpedit.DeleteGPOLink
title: DeleteGPOLink function
author: windows-sdk-content
description: The DeleteGPOLink function deletes the link between the specified GPO and the specified site, domain, or organizational unit.
old-location: policy\deletegpolink.htm
tech.root: policy
ms.assetid: e797bc8d-c0c5-4d93-b553-6c07029af01f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteGPOLink, DeleteGPOLink function [Group Policy], _win32_deletegpolink, gpedit/DeleteGPOLink, policy.deletegpolink
ms.topic: function
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gpedit.lib
req.dll: Gpedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gpedit.dll
api_name:
 - DeleteGPOLink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteGPOLink function


## -description


The
    <b>DeleteGPOLink</b> function deletes the link between the specified GPO and the specified site, domain, or organizational unit.


## -parameters




### -param lpGPO [in]

A value that specifies the path to the GPO, in ADSI format (LDAP://cn=<i>user</i>, ou=<i>users</i>, dc=<i>coname</i>, dc=<i>com</i>). You cannot specify a server name in this parameter.


### -param lpContainer [in]

Specifies the Active Directory path to the site, domain, or organizational unit.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the  header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/25d1035d-4ece-4f57-88f2-139f39dbdb86">CreateGPOLink</a>



<a href="https://msdn.microsoft.com/164b1d10-9ec0-43c8-80fe-be1ad8ec991f">DeleteAllGPOLinks</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

