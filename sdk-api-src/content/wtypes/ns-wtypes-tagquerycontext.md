---
UID: NS:wtypes.tagQUERYCONTEXT
title: tagQUERYCONTEXT
author: windows-sdk-content
description: Contains a list of attributes used to look up a class implementation.
old-location: com\querycontext.htm
old-project: com
ms.assetid: 5d6a17e1-dcdd-4691-aec2-f63dbcb26027
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: QUERYCONTEXT, QUERYCONTEXT structure [COM], _com_QUERYCONTEXT, com.querycontext, tagQUERYCONTEXT, wtypes/tagQUERYCONTEXT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QUERYCONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WTypes.h
api_name:
-	QUERYCONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagQUERYCONTEXT structure


## -description


Contains a list of attributes used to look up a class implementation.


## -struct-fields




### -field dwContext

The execution context.


### -field Platform

The operating system platform and processor architecture. For more information, see <a href="https://msdn.microsoft.com/e9ffa8ba-98a2-431c-a069-20ed4a45e6f8">CSPLATFORM</a>.


### -field Locale

The locale identifier. For more information, see <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.


### -field dwVersionHi

The high version number.


### -field dwVersionLo

The low version number.


## -see-also




<a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>



<a href="https://msdn.microsoft.com/9486ef2d-51a1-41b4-85e5-427af9a98cec">CoInstall</a>
 

 

