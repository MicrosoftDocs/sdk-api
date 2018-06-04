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

# _IMAGE_COFF_SYMBOLS_HEADER structure


## -description


Represents the COFF symbols header.


## -struct-fields




### -field NumberOfSymbols

The number of symbols.


### -field LvaToFirstSymbol

The virtual address of the first symbol.


### -field NumberOfLinenumbers

The number of line-number entries.


### -field LvaToFirstLinenumber

The virtual address of the first line-number entry.


### -field RvaToFirstByteOfCode

The relative virtual address of the first byte of code.


### -field RvaToLastByteOfCode

The relative virtual address of the last byte of code.


### -field RvaToFirstByteOfData

The relative virtual address of the first byte of data.


### -field RvaToLastByteOfData

The relative virtual address of the last byte of data.


## -see-also




<a href="https://msdn.microsoft.com/b88c7a21-933f-450c-97e8-04cf3c5f9b11">ImageHlp Structures</a>
 

 

