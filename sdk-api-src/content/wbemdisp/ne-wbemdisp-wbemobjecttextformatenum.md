---
UID: NE:wbemdisp.WbemObjectTextFormatEnum
title: WbemObjectTextFormatEnum (wbemdisp.h)
description: Define the valid object text formats to be used by SWbemObjectEx.GetText_.
helpviewer_keywords: ["WMI_OBJ_TEXT_LAST","WMI_OBJ_TEXT_WMI_EXT1","WMI_OBJ_TEXT_WMI_EXT10","WMI_OBJ_TEXT_WMI_EXT2","WMI_OBJ_TEXT_WMI_EXT3","WMI_OBJ_TEXT_WMI_EXT4","WMI_OBJ_TEXT_WMI_EXT5","WMI_OBJ_TEXT_WMI_EXT6","WMI_OBJ_TEXT_WMI_EXT7","WMI_OBJ_TEXT_WMI_EXT8","WMI_OBJ_TEXT_WMI_EXT9","WbemObjectTextFormatEnum","WbemObjectTextFormatEnum enumeration [Windows Management Instrumentation]","_hmm_wbemobjecttextformatenum","wbemObjectTextFormatCIMDTD20","wbemObjectTextFormatWMIDTD20","wbemdisp/WMI_OBJ_TEXT_LAST","wbemdisp/WMI_OBJ_TEXT_WMI_EXT1","wbemdisp/WMI_OBJ_TEXT_WMI_EXT10","wbemdisp/WMI_OBJ_TEXT_WMI_EXT2","wbemdisp/WMI_OBJ_TEXT_WMI_EXT3","wbemdisp/WMI_OBJ_TEXT_WMI_EXT4","wbemdisp/WMI_OBJ_TEXT_WMI_EXT5","wbemdisp/WMI_OBJ_TEXT_WMI_EXT6","wbemdisp/WMI_OBJ_TEXT_WMI_EXT7","wbemdisp/WMI_OBJ_TEXT_WMI_EXT8","wbemdisp/WMI_OBJ_TEXT_WMI_EXT9","wbemdisp/WbemObjectTextFormatEnum","wbemdisp/wbemObjectTextFormatCIMDTD20","wbemdisp/wbemObjectTextFormatWMIDTD20","wmi.wbemobjecttextformatenum"]
old-location: wmi\wbemobjecttextformatenum.htm
tech.root: wmi
ms.assetid: 0c97d16c-e6fc-431c-8d49-943f716a4284
ms.date: 12/05/2018
ms.keywords: WMI_OBJ_TEXT_LAST, WMI_OBJ_TEXT_WMI_EXT1, WMI_OBJ_TEXT_WMI_EXT10, WMI_OBJ_TEXT_WMI_EXT2, WMI_OBJ_TEXT_WMI_EXT3, WMI_OBJ_TEXT_WMI_EXT4, WMI_OBJ_TEXT_WMI_EXT5, WMI_OBJ_TEXT_WMI_EXT6, WMI_OBJ_TEXT_WMI_EXT7, WMI_OBJ_TEXT_WMI_EXT8, WMI_OBJ_TEXT_WMI_EXT9, WbemObjectTextFormatEnum, WbemObjectTextFormatEnum enumeration [Windows Management Instrumentation], _hmm_wbemobjecttextformatenum, wbemObjectTextFormatCIMDTD20, wbemObjectTextFormatWMIDTD20, wbemdisp/WMI_OBJ_TEXT_LAST, wbemdisp/WMI_OBJ_TEXT_WMI_EXT1, wbemdisp/WMI_OBJ_TEXT_WMI_EXT10, wbemdisp/WMI_OBJ_TEXT_WMI_EXT2, wbemdisp/WMI_OBJ_TEXT_WMI_EXT3, wbemdisp/WMI_OBJ_TEXT_WMI_EXT4, wbemdisp/WMI_OBJ_TEXT_WMI_EXT5, wbemdisp/WMI_OBJ_TEXT_WMI_EXT6, wbemdisp/WMI_OBJ_TEXT_WMI_EXT7, wbemdisp/WMI_OBJ_TEXT_WMI_EXT8, wbemdisp/WMI_OBJ_TEXT_WMI_EXT9, wbemdisp/WbemObjectTextFormatEnum, wbemdisp/wbemObjectTextFormatCIMDTD20, wbemdisp/wbemObjectTextFormatWMIDTD20, wmi.wbemobjecttextformatenum
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
targetos: Windows
req.typenames: WbemObjectTextFormatEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemObjectTextFormatEnum
 - wbemdisp/WbemObjectTextFormatEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemObjectTextFormatEnum
---

# WbemObjectTextFormatEnum enumeration


## -description

The 
WbemObjectTextFormatEnum constants define the valid object text formats to be used by 
<a href="/windows/desktop/WmiSdk/swbemobjectex-gettext-">SWbemObjectEx.GetText_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.

## -enum-fields

### -field wbemObjectTextFormatCIMDTD20:1

XML format conforming to the DMTF (Distributed Management Task Force) CIM document type definition (DTD) version 2.0.

### -field wbemObjectTextFormatWMIDTD20:2

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

<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>



<a href="/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemtextflagenum">WbemTextFlagEnum</a>
