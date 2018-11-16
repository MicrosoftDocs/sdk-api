---
UID: NS:dde.DDEPOKE
title: DDEPOKE
author: windows-sdk-content
description: Contains the data, and information about the data, sent as part of a WM_DDE_POKE message.
old-location: dataxchg\ddepoke.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangestructures\ddepoke.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CF_BITMAP, CF_DIB, CF_DIF, CF_ENHMETAFILE, CF_METAFILEPICT, CF_OEMTEXT, CF_PALETTE, CF_PENDATA, CF_RIFF, CF_SYLK, CF_TEXT, CF_TIFF, CF_UNICODETEXT, CF_WAVE, DDEPOKE, DDEPOKE structure [Data Exchange], _win32_DDEPOKE_str, _win32_ddepoke_str_cpp, dataxchg.ddepoke, dde/DDEPOKE, winui._win32_ddepoke_str
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dde.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Dde.h
api_name:
 - DDEPOKE
product: Windows
targetos: Windows
req.typenames: DDEPOKE
req.redist: 
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
 

 

