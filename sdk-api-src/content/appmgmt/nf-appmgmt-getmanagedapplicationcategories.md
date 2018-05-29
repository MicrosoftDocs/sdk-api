---
UID: NF:appmgmt.GetManagedApplicationCategories
title: GetManagedApplicationCategories function
author: windows-sdk-content
description: The GetManagedApplicationCategories function gets a list of application categories for a domain. The list is the same for all users in the domain.
old-location: policy\getmanagedapplicationcategories.htm
old-project: Policy
ms.assetid: 10824852-7810-483a-91b3-2d9cc3d21934
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: GetManagedApplicationCategories, GetManagedApplicationCategories function [Group Policy], appmgmt/GetManagedApplicationCategories, policy.getmanagedapplicationcategories
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: appmgmt.h
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
req.typenames: INSTALLSPECTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	GetManagedApplicationCategories
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# GetManagedApplicationCategories function


## -description


The
    <b>GetManagedApplicationCategories</b> function gets a list of application categories for a domain. The list is the same for all users in the domain.


## -parameters




### -param dwReserved [out]

This parameter is reserved. Its value must be 0.


### -param pAppCategory [out]

A <a href="https://msdn.microsoft.com/640aa5d0-c135-46b7-a25f-03c6325cb561">APPCATEGORYINFOLIST</a> structure that contains a list of application categories. This structure must be freed by calling <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>  when the list is no longer required.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -remarks



The structure returned by <b>GetManagedApplicationCategories</b> must be freed by calling <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> when the list is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/640aa5d0-c135-46b7-a25f-03c6325cb561">APPCATEGORYINFOLIST</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

