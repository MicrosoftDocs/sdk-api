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

# WbemCimtypeEnum enumeration


## -description


The 
WbemCimtypeEnum constants define the valid CIM types of a property value.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use the Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemCimtypeSint8

Signed 8-bit integer


### -field wbemCimtypeUint8

Unsigned 8-bit integer


### -field wbemCimtypeSint16

Signed 16-bit integer


### -field wbemCimtypeUint16

Unsigned 16-bit integer


### -field wbemCimtypeSint32

Signed 32-bit integer


### -field wbemCimtypeUint32

Unsigned 32-bit integer


### -field wbemCimtypeSint64

Signed 64-bit integer


### -field wbemCimtypeUint64

Unsigned 64-bit integer


### -field wbemCimtypeReal32

32-bit real number


### -field wbemCimtypeReal64

64-bit real number


### -field wbemCimtypeBoolean

Boolean value


### -field wbemCimtypeString

String


### -field wbemCimtypeDatetime

Date/time value


### -field wbemCimtypeReference

Reference to a CIM object


### -field wbemCimtypeChar16

16-bit character


### -field wbemCimtypeObject

CIM object


## -see-also




<a href="https://msdn.microsoft.com/ab67954c-ead2-4906-9680-503612d3f12d">CIMTYPE_ENUMERATION</a>



<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 

