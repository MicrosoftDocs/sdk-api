---
UID: NF:oledlg.OleUICanConvertOrActivateAs
title: OleUICanConvertOrActivateAs function (oledlg.h)
description: Determines if there are any OLE object classes in the registry that can be used to convert or activate the specified CLSID from.
helpviewer_keywords: ["OleUICanConvertOrActivateAs","OleUICanConvertOrActivateAs function [COM]","_ole_OleUICanConvertOrActivateAs","com.oleuicanconvertoractivateas","oledlg/OleUICanConvertOrActivateAs"]
old-location: com\oleuicanconvertoractivateas.htm
tech.root: com
ms.assetid: 9ecd978e-eded-472b-8d45-525bae56bded
ms.date: 12/05/2018
ms.keywords: OleUICanConvertOrActivateAs, OleUICanConvertOrActivateAs function [COM], _ole_OleUICanConvertOrActivateAs, com.oleuicanconvertoractivateas, oledlg/OleUICanConvertOrActivateAs
req.header: oledlg.h
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
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleUICanConvertOrActivateAs
 - oledlg/OleUICanConvertOrActivateAs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleDlg.dll
api_name:
 - OleUICanConvertOrActivateAs
---

# OleUICanConvertOrActivateAs function


## -description

Determines if there are any OLE object classes in the registry that can be used to convert or activate the specified CLSID from.

## -parameters

### -param rClsid [in]

The CLSID of the class for which the information is required.

### -param fIsLinkedObject [in]

<b>TRUE</b> if the original object is a linked object; <b>FALSE</b> otherwise.

### -param wFormat [in]

Format of the original class.

## -returns

This function returns <b>TRUE</b> if the specified class can be converted to another class; <b>FALSE</b> otherwise.

## -remarks

<b>OleUICanConvertOrActivateAs</b> searches the registry for classes that include wFormat in their \Conversion\Readable\Main, \Conversion\ReadWriteable\Main, and \DataFormats\DefaultFile entries.



This function is useful for determining if a <b>Convert...</b> menu item should be disabled. If the CF_DISABLEDISPLAYASICON flag is specified in the call to <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiconverta">OleUIConvert</a>, then the <b>Convert...</b> menu item should be enabled only if <b>OleUICanConvertOrActivateAs</b> returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiconverta">OleUIConvert</a>