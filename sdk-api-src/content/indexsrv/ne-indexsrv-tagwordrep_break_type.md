---
UID: NE:indexsrv.tagWORDREP_BREAK_TYPE
title: tagWORDREP_BREAK_TYPE
author: windows-sdk-content
description: Describes the type of break that separates the current word from the previous word.
old-location: search\wordrep_break_type.htm
tech.root: search
ms.assetid: 8E6F5DA6-F9A4-4B58-8236-F19E51AE3E8B
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WORDREP_BREAK_EOC, WORDREP_BREAK_EOP, WORDREP_BREAK_EOS, WORDREP_BREAK_EOW, WORDREP_BREAK_TYPE, indexsrv/WORDREP_BREAK_EOC, indexsrv/WORDREP_BREAK_EOP, indexsrv/WORDREP_BREAK_EOS, indexsrv/WORDREP_BREAK_EOW, indexsrv/tagWORDREP_BREAK_TYPE, search.wordrep_break_type, tagWORDREP_BREAK_TYPE, tagWORDREP_BREAK_TYPE enumeration [search]
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: indexsrv.h
req.include-header: 
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
 - indexsrv.h
api_name:
 - WORDREP_BREAK_TYPE
product: Windows
targetos: Windows
req.typenames: WORDREP_BREAK_TYPE
req.redist: 
---

# tagWORDREP_BREAK_TYPE enumeration


## -description


Describes the type of break that separates the current word from the previous word.


## -enum-fields




### -field WORDREP_BREAK_EOW

A word break is placed between this word and the previous word that was placed in the WordSink. This break is the default used by the <a href="https://msdn.microsoft.com/3D645BF6-895E-46E2-92A3-3E301CD228D8">IWordSink::PutWord</a> method.


### -field WORDREP_BREAK_EOS

A sentence break is placed between this word and the previous word.


### -field WORDREP_BREAK_EOP

A paragraph break is placed between this word and the previous word. 


### -field WORDREP_BREAK_EOC

A chapter break is placed between this word and the previous word.


## -see-also




<a href="https://msdn.microsoft.com/5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA">IWordSink::PutAltWord</a>



<a href="https://msdn.microsoft.com/C8622067-D8CE-4099-8B9F-941720F4706B">IWordSink::PutBreak</a>
 

 

