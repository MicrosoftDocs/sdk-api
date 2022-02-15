---
UID: NE:wbemdisp.WbemTextFlagEnum
title: WbemTextFlagEnum (wbemdisp.h)
description: Defines the content of generated object text and is used by SWbemObject.GetObjectText_.
helpviewer_keywords: ["WbemTextFlagEnum","WbemTextFlagEnum enumeration [Windows Management Instrumentation]","_hmm_wbemtextflagenum","wbemTextFlagNoFlavors","wbemdisp/WbemTextFlagEnum","wbemdisp/wbemTextFlagNoFlavors","wmi.wbemtextflagenum"]
old-location: wmi\wbemtextflagenum.htm
tech.root: wmi
ms.assetid: 81384e65-5ea0-420a-b92f-e93d5e545252
ms.date: 12/05/2018
ms.keywords: WbemTextFlagEnum, WbemTextFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemtextflagenum, wbemTextFlagNoFlavors, wbemdisp/WbemTextFlagEnum, wbemdisp/wbemTextFlagNoFlavors, wmi.wbemtextflagenum
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
req.typenames: WbemTextFlagEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemTextFlagEnum
 - wbemdisp/WbemTextFlagEnum
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
 - WbemTextFlagEnum
---

# WbemTextFlagEnum enumeration


## -description

The 
WbemTextFlagEnum constant defines the content of generated object text and is used by 
<a href="/windows/desktop/WmiSdk/swbemobject-getobjecttext-">SWbemObject.GetObjectText_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library;. script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.

## -enum-fields

### -field wbemTextFlagNoFlavors:0x1

Excludes qualifier flavors from the object text.

## -see-also

<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>



<a href="/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemobjecttextformatenum">WbemObjectTextFormatEnum</a>
