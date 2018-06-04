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

# _ads_class_def structure


## -description


The <b>ADS_CLASS_DEF</b> structure is used only as a part of <b>IDirectorySchemaMgmt</b>, which is an obsolete interface.  The information that follows is provided for legacy purposes only.
   

The <b>ADS_CLASS_DEF</b> structure holds the definitions of an object class.


## -struct-fields




### -field pszClassName

The null-terminated Unicode string that specifies the class name.


### -field dwMandatoryAttrs

The number of mandatory class attributes.


### -field ppszMandatoryAttrs

Pointer to an array of  null-terminated Unicode strings that contain the names of the mandatory attributes.


### -field optionalAttrs

Number of optional attributes of the class.


### -field ppszOptionalAttrs

Pointer to an array of null-terminated Unicode strings that contain the names of the optional attributes.


### -field dwNamingAttrs

Number of naming attributes.


### -field ppszNamingAttrs

Pointer to an array of null-terminated Unicode strings that contain the names of the naming attributes.


### -field dwSuperClasses

Number of super classes of an object of this class.


### -field ppszSuperClasses

Pointer to an array of null-terminated Unicode strings that contain the names of the super classes.


### -field fIsContainer

Flags that indicate the object of the class is a container when it is <b>TRUE</b> and not a container when <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 

