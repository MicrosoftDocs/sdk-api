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

# _SI_PAGE_TYPE enumeration


## -description


The <b>SI_PAGE_TYPE</b> enumeration contains values that indicate the types of property pages in an access control editor property sheet.


## -enum-fields




### -field SI_PAGE_PERM

The 
<a href="https://msdn.microsoft.com/6623fe7e-e91d-49c7-9ad0-7791c178d12b">basic security property page</a> for editing the object's DACL.


### -field SI_PAGE_ADVPERM

The 
<a href="https://msdn.microsoft.com/85a9fe30-871b-4909-b789-3fc257ffdbff">Permissions</a> tab for advanced editing of the object's DACL, such as editing object-specific ACEs.


### -field SI_PAGE_AUDIT

The 
<a href="https://msdn.microsoft.com/2a9152b7-c72d-4f03-bc3f-b75927fb4b6c">Auditing</a> tab for editing the object's SACL.


### -field SI_PAGE_OWNER

The 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn965828">Owner</a> tab for editing the object's owner.


### -field SI_PAGE_EFFECTIVE

The <b>Effective Permission</b> tab that displays the effective permissions granted to a specified user or group for access to the object.


### -field SI_PAGE_TAKEOWNERSHIP

A dialog box for changing the owner of the object.


### -field SI_PAGE_SHARE




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/9b891e64-e648-44a4-add6-d4c214394be8">ISecurityInformation::PropertySheetPageCallback</a>
 

 

