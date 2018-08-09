---
UID: NF:oledlg.OleUICanConvertOrActivateAs
title: OleUICanConvertOrActivateAs function
author: windows-sdk-content
description: Determines if there are any OLE object classes in the registry that can be used to convert or activate the specified CLSID from.
old-location: com\oleuicanconvertoractivateas.htm
old-project: com
ms.assetid: 9ecd978e-eded-472b-8d45-525bae56bded
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OleUICanConvertOrActivateAs, OleUICanConvertOrActivateAs function [COM], _ole_OleUICanConvertOrActivateAs, com.oleuicanconvertoractivateas, oledlg/OleUICanConvertOrActivateAs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: OLEUIPASTEFLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleDlg.dll
api_name:
 - OleUICanConvertOrActivateAs
product: Windows
targetos: Windows
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
req.product: ADAM
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



This function is useful for determining if a <b>Convert...</b> menu item should be disabled. If the CF_DISABLEDISPLAYASICON flag is specified in the call to <a href="https://msdn.microsoft.com/3af4b321-cea2-4f88-ae22-2dcefbb2c2ad">OleUIConvert</a>, then the <b>Convert...</b> menu item should be enabled only if <b>OleUICanConvertOrActivateAs</b> returns <b>TRUE</b>.





## -see-also




<a href="https://msdn.microsoft.com/3af4b321-cea2-4f88-ae22-2dcefbb2c2ad">OleUIConvert</a>
 

 

