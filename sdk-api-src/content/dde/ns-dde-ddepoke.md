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

# DDEPOKE structure


## -description


Contains the data, and information about the data, sent as part of a <a href="https://msdn.microsoft.com/848142b7-a7ef-4206-9bb3-b511388cfaaa">WM_DDE_POKE</a> message. 


## -struct-fields




### -field unused

Type: <b>unsigned short</b>

Unused.


### -field fRelease

Type: <b>unsigned short</b>

Indicates whether the application receiving the <a href="https://msdn.microsoft.com/848142b7-a7ef-4206-9bb3-b511388cfaaa">WM_DDE_POKE</a> message should free the data. If this value is nonzero, the application should free the data. 


### -field fReserved

Type: <b>unsigned short</b>

Reserved.


### -field usFlags

 


### -field cfFormat

Type: <b>short</b>

The format of the data. The format should be a standard or registered clipboard format. The following standard clipboard formats can be used: 
                



#### CF_BITMAP (2)



#### CF_DIB (8)



#### CF_DIF (5)



#### CF_ENHMETAFILE (14)



#### CF_METAFILEPICT (3)



#### CF_OEMTEXT (7)



#### CF_PALETTE (9)



#### CF_PENDATA (10)



#### CF_RIFF (11)



#### CF_SYLK (4)



#### CF_TEXT (1)



#### CF_TIFF (6)



#### CF_WAVE (12)



#### CF_UNICODETEXT (13)


### -field Value

Type: <b>BYTE[1]</b>

Contains the data. The length and type of data depend on the value of the 
					<b>cfFormat</b> member. 


## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/848142b7-a7ef-4206-9bb3-b511388cfaaa">WM_DDE_POKE</a>
 

 

