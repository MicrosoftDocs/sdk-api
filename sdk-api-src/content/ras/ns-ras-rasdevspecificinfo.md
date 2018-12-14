---
UID: NS:ras.tagRASDEVSPECIFICINFO
title: RASDEVSPECIFICINFO
author: windows-sdk-content
description: Used to send a cookie for server validation and bypass point-to-point (PPP) authentication.
old-location: rras\rasdevspecificinfo.htm
tech.root: rras
ms.assetid: 0dee3f10-d49b-4059-8cfb-c28af6b8b371
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PRASDEVSPECIFICINFO, PRASDEVSPECIFICINFO, PRASDEVSPECIFICINFO structure pointer [RAS], RASDEVSPECIFICINFO, RASDEVSPECIFICINFO structure [RAS], ras/PRASDEVSPECIFICINFO, ras/RASDEVSPECIFICINFO, rras.rasdevspecificinfo"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Ras.h
api_name:
 - RASDEVSPECIFICINFO
product: Windows
targetos: Windows
req.typenames: RASDEVSPECIFICINFO, *PRASDEVSPECIFICINFO
req.redist: 
---

# RASDEVSPECIFICINFO structure


## -description


The <b>RASDEVSPECIFICINFO</b> structure is used to send a cookie for server validation and bypass point-to-point (PPP) authentication.


## -struct-fields




### -field dwSize

The size, in bytes, of the cookie in <b>pbDevSpecificInfo</b>.


### -field pbDevSpecificInfo

A pointer to a BLOB that contains the authentication cookie.


## -see-also




<a href="https://msdn.microsoft.com/533c9ab4-69d0-492d-81c6-2c07ca219fc7">RASDIALEXTENSIONS</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/c20e8892-7c5e-48cc-939a-9b747fefe09d">Remote Access Service Structures</a>
 

 

