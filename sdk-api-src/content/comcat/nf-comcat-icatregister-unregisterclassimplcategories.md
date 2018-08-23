---
UID: NF:comcat.ICatRegister.UnRegisterClassImplCategories
title: ICatRegister::UnRegisterClassImplCategories
author: windows-sdk-content
description: Removes one or more implemented category identifiers from a class.
old-location: com\icatregister_unregisterclassimplcategories.htm
old-project: com
ms.assetid: 4a227fd1-6cbc-4354-a3e2-04aceb73ab65
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICatRegister interface [COM],UnRegisterClassImplCategories method, ICatRegister.UnRegisterClassImplCategories, ICatRegister::UnRegisterClassImplCategories, UnRegisterClassImplCategories, UnRegisterClassImplCategories method [COM], UnRegisterClassImplCategories method [COM],ICatRegister interface, _com_icatregister_unregisterclassimplcategories, com.icatregister_unregisterclassimplcategories, comcat/ICatRegister::UnRegisterClassImplCategories
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comcat.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ServerInformation, *PServerInformation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - ICatRegister.UnRegisterClassImplCategories
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatRegister::UnRegisterClassImplCategories


## -description


Removes one or more implemented category identifiers from a class.


## -parameters




### -param rclsid [in]

The class identifier.


### -param cCategories [in]

The number of category CATIDs to be removed.


### -param rgcatid [in]

An array of CATIDs that are to be removed. Only the category IDs specified in this array are removed.


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



In case of an error, this method does not ensure that the registry is restored to the state prior to the call. This method will be successful even if one or more of the category IDs specified are not registered for the class. This method can only be called by the owner of a class, usually as part of the de-installation of the component.




## -see-also




<a href="https://msdn.microsoft.com/3f4f9beb-51db-407f-91ea-6e32ff5796ce">ICatRegister</a>
 

 

