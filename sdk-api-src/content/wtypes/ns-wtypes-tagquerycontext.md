---
UID: NS:wtypes.tagQUERYCONTEXT
title: tagQUERYCONTEXT
author: windows-sdk-content
description: Contains a list of attributes used to look up a class implementation.
old-location: winprog\querycontext.htm
tech.root: DevNotes
ms.assetid: 8b27c090-2bae-4511-9be8-4bc077295ac5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: QUERYCONTEXT, QUERYCONTEXT structure [Windows API], tagQUERYCONTEXT, winprog.querycontext, wtypes/tagQUERYCONTEXT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtypes.idl
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
 - wtypes.h
api_name:
 - QUERYCONTEXT
product: Windows
targetos: Windows
req.typenames: QUERYCONTEXT
req.redist: 
---

# tagQUERYCONTEXT structure


## -description


Contains a list of attributes used to look up a class implementation.


## -struct-fields




### -field dwContext

The execution context.


### -field Platform

The operating system platform and processor architecture. For more information, see <a href="https://msdn.microsoft.com/cb8b4615-427d-4277-ad4b-c9988c3e1be7">CSPLATFORM</a>.


### -field Locale

The locale ID.


### -field dwVersionHi

The high version number.


### -field dwVersionLo

The low version number.


## -see-also




<a href="https://msdn.microsoft.com/cb8b4615-427d-4277-ad4b-c9988c3e1be7">CSPLATFORM</a>



<a href="https://msdn.microsoft.com/92b290a5-0923-42fc-8231-1decca26adc1">CoInstall</a>
 

 

