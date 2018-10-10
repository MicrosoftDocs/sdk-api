---
UID: NE:wbemdisp.WbemObjectTextFormatEnum
title: WbemObjectTextFormatEnum
author: windows-sdk-content
description: Define the valid object text formats to be used by SWbemObjectEx.GetText_.
old-location: wmi\wbemobjecttextformatenum.htm
tech.root: WmiSdk
ms.assetid: 0c97d16c-e6fc-431c-8d49-943f716a4284
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: WMI_OBJ_TEXT_LAST, WMI_OBJ_TEXT_WMI_EXT1, WMI_OBJ_TEXT_WMI_EXT10, WMI_OBJ_TEXT_WMI_EXT2, WMI_OBJ_TEXT_WMI_EXT3, WMI_OBJ_TEXT_WMI_EXT4, WMI_OBJ_TEXT_WMI_EXT5, WMI_OBJ_TEXT_WMI_EXT6, WMI_OBJ_TEXT_WMI_EXT7, WMI_OBJ_TEXT_WMI_EXT8, WMI_OBJ_TEXT_WMI_EXT9, WbemObjectTextFormatEnum, WbemObjectTextFormatEnum enumeration [Windows Management Instrumentation], _hmm_wbemobjecttextformatenum, wbemObjectTextFormatCIMDTD20, wbemObjectTextFormatWMIDTD20, wbemdisp/WMI_OBJ_TEXT_LAST, wbemdisp/WMI_OBJ_TEXT_WMI_EXT1, wbemdisp/WMI_OBJ_TEXT_WMI_EXT10, wbemdisp/WMI_OBJ_TEXT_WMI_EXT2, wbemdisp/WMI_OBJ_TEXT_WMI_EXT3, wbemdisp/WMI_OBJ_TEXT_WMI_EXT4, wbemdisp/WMI_OBJ_TEXT_WMI_EXT5, wbemdisp/WMI_OBJ_TEXT_WMI_EXT6, wbemdisp/WMI_OBJ_TEXT_WMI_EXT7, wbemdisp/WMI_OBJ_TEXT_WMI_EXT8, wbemdisp/WMI_OBJ_TEXT_WMI_EXT9, wbemdisp/WbemObjectTextFormatEnum, wbemdisp/wbemObjectTextFormatCIMDTD20, wbemdisp/wbemObjectTextFormatWMIDTD20, wmi.wbemobjecttextformatenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
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
 - Wbemdisp.h
api_name:
 - WbemObjectTextFormatEnum
product: Windows
targetos: Windows
req.typenames: WbemObjectTextFormatEnum
req.redist: 
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
 

 

