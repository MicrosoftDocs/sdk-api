---
UID: NS:appmgmt._APPCATEGORYINFOLIST
title: "_APPCATEGORYINFOLIST"
author: windows-driver-content
description: The APPCATEGORYINFOLIST structure contains a list of APPCATEGORYINFO structures, one for each category in the domain. This structure can be returned by the GetManagedApplicationCategories function.
old-location: policy\appcategoryinfolist_str.htm
old-project: Policy
ms.assetid: 640aa5d0-c135-46b7-a25f-03c6325cb561
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: APPCATEGORYINFOLIST, APPCATEGORYINFOLIST structure [Group Policy], PAPPCATEGORYINFOLIST, PAPPCATEGORYINFOLIST structure pointer [Group Policy], _APPCATEGORYINFOLIST, appmgmt/APPCATEGORYINFOLIST, appmgmt/PAPPCATEGORYINFOLIST, policy.appcategoryinfolist_str
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
req.typenames: APPCATEGORYINFOLIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Appmgmt.h
api_name:
-	APPCATEGORYINFOLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _APPCATEGORYINFOLIST structure


## -description


The <b>APPCATEGORYINFOLIST</b> structure contains a list of <a href="https://msdn.microsoft.com/a03f6617-2b55-4d63-85eb-421d7c5494da">APPCATEGORYINFO</a> structures, one for each category in the domain. This structure can be returned by the  <a href="https://msdn.microsoft.com/10824852-7810-483a-91b3-2d9cc3d21934">GetManagedApplicationCategories</a> function.


## -struct-fields




### -field cCategory

The number of categories listed in the <i>pCategoryInfo</i>.


### -field pCategoryInfo

An array of <a href="https://msdn.microsoft.com/a03f6617-2b55-4d63-85eb-421d7c5494da">APPCATEGORYINFO</a> structures, one for each category in the domain.


## -see-also




<a href="https://msdn.microsoft.com/a03f6617-2b55-4d63-85eb-421d7c5494da">APPCATEGORYINFO</a>



<a href="https://msdn.microsoft.com/10824852-7810-483a-91b3-2d9cc3d21934">GetManagedApplicationCategories</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>
 

 

