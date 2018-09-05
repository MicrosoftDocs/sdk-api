---
UID: NF:comcat.ICatRegister.UnRegisterClassReqCategories
title: ICatRegister::UnRegisterClassReqCategories
author: windows-sdk-content
description: Removes one or more required category identifiers from a class.
old-location: com\icatregister_unregisterclassreqcategories.htm
old-project: com
ms.assetid: d957bc13-f5f7-4cb3-925e-4867ba9622cd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICatRegister interface [COM],UnRegisterClassReqCategories method, ICatRegister.UnRegisterClassReqCategories, ICatRegister::UnRegisterClassReqCategories, UnRegisterClassReqCategories, UnRegisterClassReqCategories method [COM], UnRegisterClassReqCategories method [COM],ICatRegister interface, _com_icatregister_unregisterclassreqcategories, com.icatregister_unregisterclassreqcategories, comcat/ICatRegister::UnRegisterClassReqCategories
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
 - ICatRegister.UnRegisterClassReqCategories
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatRegister::UnRegisterClassReqCategories


## -description


Removes one or more required category identifiers from a class.


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



In case of an error, this method does not ensure that the registry is restored to the state prior to the call. This method will be successful even if one or more of the category IDs specified are not registered for the class.




## -see-also




<a href="https://msdn.microsoft.com/3f4f9beb-51db-407f-91ea-6e32ff5796ce">ICatRegister</a>
 

 

