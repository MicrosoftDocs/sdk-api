---
UID: NS:lpmapi.IntServServiceHdr
title: IntServServiceHdr
author: windows-sdk-content
description: The IntServServiceHdr structure is a header for Integrated Services service objects.
old-location: qos\intservservicehdr.htm
old-project: QOS
ms.assetid: 63e6a944-f16e-4b90-ab77-22e5c8ef3fb2
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IntServServiceHdr, IntServServiceHdr structure [QOS], lpmapi/IntServServiceHdr, qos.intservservicehdr
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IntServServiceHdr
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a>



<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>
 

 

