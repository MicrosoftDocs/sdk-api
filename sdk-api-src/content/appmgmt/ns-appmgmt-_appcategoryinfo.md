---
UID: NS:appmgmt._APPCATEGORYINFO
title: "_APPCATEGORYINFO"
author: windows-driver-content
description: The APPCATEGORYINFO structure contains information about an application.
old-location: policy\appcategoryinfo_str.htm
old-project: Policy
ms.assetid: a03f6617-2b55-4d63-85eb-421d7c5494da
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: APPCATEGORYINFO, APPCATEGORYINFO structure [Group Policy], _APPCATEGORYINFO, appmgmt/APPCATEGORYINFO, policy.appcategoryinfo_str
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: APPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Appmgmt.h
api_name:
-	APPCATEGORYINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _APPCATEGORYINFO structure


## -description


The  <b>APPCATEGORYINFO</b> structure contains information about an application. The <a href="https://msdn.microsoft.com/640aa5d0-c135-46b7-a25f-03c6325cb561">APPCATEGORYINFOLIST</a> structure contains a list of <b>APPCATEGORYINFO</b> structures, one for each category in the domain. The <b>APPCATEGORYINFOLIST</b> structure can be returned by the  <a href="https://msdn.microsoft.com/10824852-7810-483a-91b3-2d9cc3d21934">GetManagedApplicationCategories</a> function.


## -struct-fields




### -field Locale

This member is unused.


### -field pszDescription

The user-friendly name of the category.


### -field AppCategoryId

The GUID identifier for this category.


## -see-also




<a href="https://msdn.microsoft.com/640aa5d0-c135-46b7-a25f-03c6325cb561">APPCATEGORYINFOLIST</a>



<a href="https://msdn.microsoft.com/10824852-7810-483a-91b3-2d9cc3d21934">GetManagedApplicationCategories</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>
 

 

