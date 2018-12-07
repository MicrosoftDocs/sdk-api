---
UID: NS:msime._IMESHF
title: "_IMESHF"
author: windows-sdk-content
description: The header of an opened user dictionary file. Used to get the user dictionary's properties, such as version, title, description, and copyright.
old-location: intl\imeshf.htm
tech.root: Intl
ms.assetid: CFFEFEDC-F614-4DD4-B1A1-4D236339E817
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMESHF, IMESHF structure [Internationalization for Windows Applications], PIMESHF, PIMESHF structure pointer [Internationalization for Windows Applications], _IMESHF, intl.imeshf, msime/IMESHF, msime/PIMESHF
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: msime.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msime.h
api_name:
 - IMESHF
product: Windows
targetos: Windows
req.typenames: IMESHF
req.redist: 
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
 

 

