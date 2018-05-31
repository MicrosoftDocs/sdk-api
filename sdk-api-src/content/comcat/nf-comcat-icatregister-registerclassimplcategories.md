---
UID: NF:comcat.ICatRegister.RegisterClassImplCategories
title: ICatRegister::RegisterClassImplCategories
author: windows-sdk-content
description: Registers the class as implementing one or more component categories.
old-location: com\icatregister_registerclassimplcategories.htm
old-project: com
ms.assetid: c293038f-4dbf-40af-9237-c9bb59c84252
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ICatRegister interface [COM],RegisterClassImplCategories method, ICatRegister.RegisterClassImplCategories, ICatRegister::RegisterClassImplCategories, RegisterClassImplCategories, RegisterClassImplCategories method [COM], RegisterClassImplCategories method [COM],ICatRegister interface, _com_icatregister_registerclassimplcategories, com.icatregister_registerclassimplcategories, comcat/ICatRegister::RegisterClassImplCategories
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ServerInformation, *PServerInformation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComCat.h
api_name:
-	ICatRegister.RegisterClassImplCategories
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatRegister::RegisterClassImplCategories


## -description


Registers the class as implementing one or more component categories.


## -parameters




### -param rclsid [in]

The class identifier.


### -param cCategories [in]

The number of categories to be associated as category identifiers for the class.


### -param rgcatid [in]

An array of CATIDs to associate as category identifiers for the class.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are incorrect.

</td>
</tr>
</table>
 




## -remarks



In case of an error, this method does not ensure that the registry is restored to the state prior to the call. This method can only be called by the owner of a class, usually as part of the installation of the component.




## -see-also




<a href="https://msdn.microsoft.com/3f4f9beb-51db-407f-91ea-6e32ff5796ce">ICatRegister</a>
 

 

