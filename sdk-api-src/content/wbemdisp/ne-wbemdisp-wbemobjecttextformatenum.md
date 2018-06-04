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

# WbemObjectTextFormatEnum enumeration


## -description


The 
WbemObjectTextFormatEnum constants define the valid object text formats to be used by 
<a href="https://msdn.microsoft.com/98961d94-8360-4ed7-b1b1-20b4fca45d45">SWbemObjectEx.GetText_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemObjectTextFormatCIMDTD20

XML format conforming to the DMTF (Distributed Management Task Force) CIM document type definition (DTD) version 2.0.


### -field wbemObjectTextFormatWMIDTD20

XML format as defined by the extended WMI version of DMTF CIM DTD version 2.0. Using this value enables WMI-specific extensions, such as embedded objects or scope.


#### - WMI_OBJ_TEXT_LAST

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT1

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT10

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT2

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT3

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT4

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT5

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT6

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT7

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT8

Not supported.


#### - WMI_OBJ_TEXT_WMI_EXT9

Not supported.


## -see-also




<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>



<a href="https://msdn.microsoft.com/81384e65-5ea0-420a-b92f-e93d5e545252">WbemTextFlagEnum</a>
 

 

