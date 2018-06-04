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

# tagDVD_SUBPICTURE_LANG_EXT enumeration


## -description



Defines the possible language extensions in a specified subpicture stream.




## -enum-fields




### -field DVD_SP_EXT_NotSpecified

Indicates that no language extensions are present.


### -field DVD_SP_EXT_Caption_Normal

Indicates that the specified stream contains normal captions.


### -field DVD_SP_EXT_Caption_Big

Indicates that the specified stream contains big captions.


### -field DVD_SP_EXT_Caption_Children

Indicates that the specified stream contains captions for children.


### -field DVD_SP_EXT_CC_Normal

Indicates that the specified stream contains normal closed captions.


### -field DVD_SP_EXT_CC_Big

Indicates that the specified stream contains big closed captions.


### -field DVD_SP_EXT_CC_Children

Indicates that the specified stream contains closed captions for children.


### -field DVD_SP_EXT_Forced

Indicates that the subpicture stream is forcedly activated, meaning that the application will not be able to turn it off.


### -field DVD_SP_EXT_DirectorComments_Normal

Indicates that the specified stream contains normal-sized director's comments.


### -field DVD_SP_EXT_DirectorComments_Big

Indicates that the specified stream contains large-sized director's comments.


### -field DVD_SP_EXT_DirectorComments_Children


            Indicates that the specified stream contains director's comments for children. 
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/f49698cd-cc83-4f05-991d-2b3bba77c33a">IDvdControl2::SelectDefaultSubpictureLanguage</a>



<a href="https://msdn.microsoft.com/ada423a5-90ef-48e1-80fa-04d0a24da8f7">IDvdInfo2::GetDefaultSubpictureLanguage</a>
 

 

