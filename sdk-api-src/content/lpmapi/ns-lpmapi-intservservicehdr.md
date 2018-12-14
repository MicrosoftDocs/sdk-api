---
UID: NS:lpmapi.__unnamed_struct_16
title: IntServServiceHdr
author: windows-sdk-content
description: The IntServServiceHdr structure is a header for Integrated Services service objects.
old-location: qos\intservservicehdr.htm
tech.root: QOS
ms.assetid: 63e6a944-f16e-4b90-ab77-22e5c8ef3fb2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IntServServiceHdr, IntServServiceHdr structure [QOS], lpmapi/IntServServiceHdr, qos.intservservicehdr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lpmapi.h
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
 - Lpmapi.h
api_name:
 - IntServServiceHdr
product: Windows
targetos: Windows
req.typenames: IntServServiceHdr
req.redist: 
---

# IntServServiceHdr structure


## -description


The 
<b>IntServServiceHdr</b> structure is a header for Integrated Services service objects.


## -struct-fields




### -field issh_service

Service number of the attached object.


### -field issh_flags

Flags for the corresponding service object.


### -field issh_len32b

Number of 32-bit WORDs in the object, excluding this header object.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa373722(v=VS.85).aspx">IntServMainHdr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373723(v=VS.85).aspx">IntServParmHdr</a>
 

 

