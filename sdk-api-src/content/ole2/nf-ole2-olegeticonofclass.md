---
UID: NF:ole2.OleGetIconOfClass
title: OleGetIconOfClass function (ole2.h)
description: Returns a handle to a metafile containing an icon and a string label for the specified CLSID.
helpviewer_keywords: ["OleGetIconOfClass","OleGetIconOfClass function [COM]","_com_OleGetIconOfClass","com.olegeticonofclass","ole2/OleGetIconOfClass"]
old-location: com\olegeticonofclass.htm
tech.root: com
ms.assetid: 88ac1c14-b5a8-4100-9fa5-d7af35052b48
ms.date: 12/05/2018
ms.keywords: OleGetIconOfClass, OleGetIconOfClass function [COM], _com_OleGetIconOfClass, com.olegeticonofclass, ole2/OleGetIconOfClass
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleGetIconOfClass
 - ole2/OleGetIconOfClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleGetIconOfClass
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleGetIconOfClass function


## -description

Returns a handle to a metafile containing an icon and a string label for the specified CLSID.

## -parameters

### -param rclsid [in]

The CLSID for which the icon and string are to be requested.

### -param lpszLabel [in, optional]

A pointer to the label for the icon.

### -param fUseTypeAsLabel [in]

Indicates whether to use the user type string in the CLSID as the icon label.

## -returns

If the function succeeds, the return value is a handle to a metafile that contains and icon and label for the specified CLSID. Otherwise, the function returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olegeticonoffile">OleGetIconOfFile</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olemetafilepictfromiconandlabel">OleMetafilePictFromIconAndLabel</a>
