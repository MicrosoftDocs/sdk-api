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

# _IMESHF structure


## -description


The header of an opened user dictionary file. Used to get the user dictionary's properties, such as version, title, description, and copyright.


## -struct-fields




### -field cbShf

The size of this structure. You must set this value before using the structure.


### -field verDic

Dictionary version.


### -field szTitle

Dictionary title.


### -field szDescription

Dictionary description.


### -field szCopyright

Dictionary copyright information.


## -see-also




<a href="https://msdn.microsoft.com/218DEE1C-945A-4CD8-BAD5-12F904FAB2DD">IFEDictionary::Create</a>



<a href="https://msdn.microsoft.com/DA710A33-BCBC-47B8-857F-5E6DF142C433">IFEDictionary::GetHeader</a>



<a href="https://msdn.microsoft.com/7170EED5-0D96-4314-8B9F-A019052B0F32">IFEDictionary::Open</a>



<a href="https://msdn.microsoft.com/8666DDE7-D90E-4423-984B-EF526FC34320">IFEDictionary::SetHeader</a>
 

 

