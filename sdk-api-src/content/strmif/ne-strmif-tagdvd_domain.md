---
UID: NE:strmif.tagDVD_DOMAIN
title: tagDVD_DOMAIN
author: windows-sdk-content
description: Defines the DVD domains.
old-location: dshow\dvd_domain.htm
old-project: DirectShow
ms.assetid: 2763a159-d4de-44c2-905b-5828f328cbd2
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: DVD_DOMAIN, DVD_DOMAIN , DVD_DOMAIN enumeration [DirectShow], DVD_DOMAINEnumeration, DVD_DOMAIN_FirstPlay, DVD_DOMAIN_Stop, DVD_DOMAIN_Title, DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, dshow.dvd_domain, strmif/DVD_DOMAIN, strmif/DVD_DOMAIN_FirstPlay, strmif/DVD_DOMAIN_Stop, strmif/DVD_DOMAIN_Title, strmif/DVD_DOMAIN_VideoManagerMenu, strmif/DVD_DOMAIN_VideoTitleSetMenu, tagDVD_DOMAIN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: DVD_DOMAIN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_DOMAIN
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
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
 

 

