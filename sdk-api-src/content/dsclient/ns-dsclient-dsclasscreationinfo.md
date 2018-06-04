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

# DSCLASSCREATIONINFO structure


## -description


The <b>DSCLASSCREATIONINFO</b> structure is used with the <a href="https://msdn.microsoft.com/23b88707-c4c3-47dd-a5bc-e325142602f5">IDsDisplaySpecifier::GetClassCreationInfo</a> method to hold data about the class creation wizard objects for an object class.


## -struct-fields




### -field dwFlags

Contains a set of flags that indicate which members of this structure contain valid data. This can be a combination of one or more of the following values.



#### DSCCIF_HASWIZARDDIALOG

The <b>clsidWizardDialog</b> member is valid.



#### DSCCIF_HASWIZARDPRIMARYPAGE

The <b>clsidWizardPrimaryPage</b> member is valid.


### -field clsidWizardDialog

Contains the class identifier of the class creation wizard dialog box. This member is not used if <b>dwFlags</b> does not contain <b>DSCCIF_HASWIZARDDIALOG</b>.


### -field clsidWizardPrimaryPage

Contains the class identifier of the primary property page of the class creation wizard. This member is not used if <b>dwFlags</b> does not contain <b>DSCCIF_HASWIZARDPRIMARYPAGE</b>.


### -field cWizardExtensions

Contains the number of elements in the <b>aWizardExtensions</b> array.


### -field aWizardExtensions

Contains an array of the class identifiers of the  property page extensions. <b>cWizardExtensions</b> specifies the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Display Structures in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/23b88707-c4c3-47dd-a5bc-e325142602f5">IDsDisplaySpecifier::GetClassCreationInfo</a>
 

 

