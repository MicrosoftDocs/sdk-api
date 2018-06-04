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

# LoadStringByReference function


## -description


Unsupported. <b>LoadStringByReference</b> may be altered or unavailable. Instead, use <a href="https://msdn.microsoft.com/f0265cd8-deb8-4bca-b379-39aff49c7df1">SHLoadIndirectString</a>.


## -parameters




### -param Flags [in]

Reserved.


### -param Language [in, optional]

The language.


### -param SourceString [in]

The source string reference.


### -param Buffer [out, optional]

The buffer to receive the string.


### -param cchBuffer [in]

The size of <i>Buffer</i>, in characters.


### -param Directory [in, optional]

The directory path to <i>SourceString</i>.


### -param pcchBufferOut [out, optional]

The number of characters written to <i>Buffer</i>.


## -returns



A <b>BOOL</b> datatype.




## -remarks



<b>LoadStringByReference</b> is not supported and may be altered or unavailable in the future. Instead, use <a href="https://msdn.microsoft.com/f0265cd8-deb8-4bca-b379-39aff49c7df1">SHLoadIndirectString</a>.



