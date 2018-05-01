---
UID: NS:cmnquery.CQFORM
title: CQFORM
author: windows-driver-content
description: Used to define a query form added to the query dialog box with the CQAddFormsProc callback function.
old-location: ad\cqform.htm
old-project: AD
ms.assetid: 65cf2e9c-8f88-4e84-8bf2-2b0fd246a835
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: "*LPCQFORM, CQFF_ISOPTIONAL, CQFF_NOGLOBALPAGES, CQFORM, CQFORM structure [Active Directory], LPCQFORM, LPCQFORM structure pointer [Active Directory], _glines_cqform, ad.cqform, cmnquery/CQFORM, cmnquery/LPCQFORM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: cmnquery.h
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
req.typenames: CQFORM, *LPCQFORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Cmnquery.h
api_name:
-	CQFORM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

