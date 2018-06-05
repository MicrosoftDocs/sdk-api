---
UID: NE:codecapi.eAVEncMPVIntraVLCTable
title: eAVEncMPVIntraVLCTable
author: windows-sdk-content
description: Specifies which variable-length coding (VLC) table to use for entropy coding. This enumeration is used with the AVEncMPVIntraVLCTable property.
old-location: dshow\eavencmpvintravlctable.htm
old-project: DirectShow
ms.assetid: 132887a8-c1f6-47f2-9c8d-aa62560b0f8a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: codecapi/eAVEncMPVIntraVLCTable, codecapi/eAVEncMPVIntraVLCTable_Alternate, codecapi/eAVEncMPVIntraVLCTable_Auto, codecapi/eAVEncMPVIntraVLCTable_MPEG1, dshow.eavencmpvintravlctable, eAVEncMPVIntraVLCTable, eAVEncMPVIntraVLCTable enumeration [DirectShow], eAVEncMPVIntraVLCTableEnumeration, eAVEncMPVIntraVLCTable_Alternate, eAVEncMPVIntraVLCTable_Auto, eAVEncMPVIntraVLCTable_MPEG1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	codecapi.h
api_name:
-	eAVEncMPVIntraVLCTable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVEncMPVIntraVLCTable enumeration


## -description



Specifies which variable-length coding (VLC) table to use for entropy coding. This enumeration is used with the <a href="https://msdn.microsoft.com/caa17027-8f11-47d3-83da-7ca83b27c978">AVEncMPVIntraVLCTable</a> property.




## -enum-fields




### -field eAVEncMPVIntraVLCTable_Auto

The encoder selects the VLC table.


### -field eAVEncMPVIntraVLCTable_MPEG1

The encoder uses the MPEG-1 VLC table.


### -field eAVEncMPVIntraVLCTable_Alternate

The encoder uses the alternate "intra" VLC table for MPEG-2.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

