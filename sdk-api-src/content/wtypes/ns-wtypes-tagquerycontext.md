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
 

 

