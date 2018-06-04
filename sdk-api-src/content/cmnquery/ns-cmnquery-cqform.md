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

# CQFORM structure


## -description


The <b>CQFORM</b> structure is used to define a query form added to the query dialog box with the <a href="https://msdn.microsoft.com/e4221299-93de-4747-b464-0d152d6e767b">CQAddFormsProc</a> callback function.


## -struct-fields




### -field cbStruct

Contains the size, in bytes, of the structure.


### -field dwFlags

Contains a set of flags that modify the behavior of the query form. This can be zero or a combination of one or more of the following values.



#### CQFF_ISOPTIONAL

Specifies that this query form is optional and is only displayed if optional forms are requested.



#### CQFF_NOGLOBALPAGES

Specifies that this form should not have the global pages added to it.


### -field clsid

Contains  the class identifier used to identify the query form.


### -field hIcon

Contains the  handle of the icon to be displayed with the query form.


### -field pszTitle

Pointer to a null-terminated Unicode string that contains the title of the query form.


## -see-also




<a href="https://msdn.microsoft.com/e4221299-93de-4747-b464-0d152d6e767b">CQAddFormsProc</a>



<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Display Structures in Active
  Directory Domain Services</a>



<a href="https://msdn.microsoft.com/fadaa7e6-ccf2-42cd-a26e-19db107ce56c">IQueryForm::AddForms</a>
 

 

