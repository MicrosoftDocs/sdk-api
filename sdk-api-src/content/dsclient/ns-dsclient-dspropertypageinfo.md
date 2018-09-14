---
UID: NS:dsclient.DSPROPERTYPAGEINFO
title: DSPROPERTYPAGEINFO
author: windows-sdk-content
description: The DSPROPERTYPAGEINFO structure is used by an Active Directory property sheet extension to obtain static registration data for the extension. This structure is supplied by the CFSTR_DSPROPERTYPAGEINFO clipboard format.
old-location: ad\dspropertypageinfo.htm
tech.root: ad
ms.assetid: 1f8313cd-5cbe-440b-bcf9-de835f2b4f4a
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: "*LPDSPROPERTYPAGEINFO, DSPROPERTYPAGEINFO, DSPROPERTYPAGEINFO structure [Active Directory], LPDSPROPERTYPAGEINFO, LPDSPROPERTYPAGEINFO structure pointer [Active Directory], _glines_dspropertypageinfo, ad.dspropertypageinfo, dsclient/DSPROPERTYPAGEINFO, dsclient/LPDSPROPERTYPAGEINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dsclient.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DSPROPERTYPAGEINFO
product: Windows
targetos: Windows
req.typenames: DSPROPERTYPAGEINFO, *LPDSPROPERTYPAGEINFO
req.redist: 
---

# DSPROPERTYPAGEINFO structure


## -description


The <b>DSPROPERTYPAGEINFO</b> structure is used by an Active Directory property sheet extension to obtain static registration data for the extension. This structure is  supplied by the <a href="https://msdn.microsoft.com/84ed1322-fee3-44ee-873e-57586261ff62">CFSTR_DSPROPERTYPAGEINFO</a> clipboard format.


## -struct-fields




### -field offsetString

Contains the offset, in bytes, from the start of the <b>DSPROPERTYPAGEINFO</b> structure to a NULL-terminated, Unicode string that contains the optional data stored for the extension.


## -remarks



The  <b>DSPROPETYPAGEINFO</b> structure contains the optional string that the extension added to the <b>adminPropertySheet</b> and/or <b>shellPropertySheet</b> attributes when the extension was registered. For more information about how this string is set, see <a href="https://msdn.microsoft.com/e2d6142b-c2fe-4435-b4af-83f7cd45218b">Registering the Property Page COM Object in a Display Specifier</a>.




## -see-also




<a href="https://msdn.microsoft.com/84ed1322-fee3-44ee-873e-57586261ff62">CFSTR_DSPROPERTYPAGEINFO</a>



<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Display Structures in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/e2d6142b-c2fe-4435-b4af-83f7cd45218b">Registering the Property Page COM Object in a Display Specifier</a>
 

 

