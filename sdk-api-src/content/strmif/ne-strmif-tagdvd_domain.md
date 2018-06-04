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

# tagDVD_DOMAIN enumeration


## -description



Defines the DVD domains.




## -enum-fields




### -field DVD_DOMAIN_FirstPlay


            Performing default initialization of a DVD disc.
          


### -field DVD_DOMAIN_VideoManagerMenu


            Displaying menus for whole disc.
          


### -field DVD_DOMAIN_VideoTitleSetMenu


            Displaying menus for current title set.
          


### -field DVD_DOMAIN_Title


            Displaying the current title.
          


### -field DVD_DOMAIN_Stop


            The DVD Navigator is in the DVD Stop domain.
          


## -remarks



This enumeration is used in the <a href="https://msdn.microsoft.com/ad850402-7b48-4517-a55f-42cfa75d3ee6">IDvdInfo2::GetCurrentDomain</a> method.

A domain is a logical space on a DVD disc. When the DVD Navigator is displaying the disc's main menu, it is said to be in the Video Manager domain. When it is displaying a menu specific to a title, it is in the Video Title Set domain. When it is playing video, it is the Title domain. When the user issues a Stop command, the Navigator goes into the Stop domain.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/ad850402-7b48-4517-a55f-42cfa75d3ee6">IDvdInfo2::GetCurrentDomain</a>
 

 

