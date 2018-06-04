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

# tagEMRSETICMPROFILE structure


## -description



The <b>EMRSETICMPROFILE</b> structure contains members for the <a href="https://msdn.microsoft.com/c95f6536-9377-4766-9eb6-004a41bcf6c5">SetICMProfile</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field dwFlags

The profile flags. This member can be SETICMPROFILE_EMBEDED (0x00000001).


### -field cbName

The size of the desired profile name.


### -field cbData

The size of profile data, if attached.


### -field Data

An array that contains the profile data. The length of this array is <b>cbName</b> plus <b>cbData</b>.


## -remarks



This structure is to be used during metafile playback.




## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/c95f6536-9377-4766-9eb6-004a41bcf6c5">SetICMProfile</a>
 

 

