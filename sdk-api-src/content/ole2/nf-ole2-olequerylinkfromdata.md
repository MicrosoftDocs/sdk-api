---
UID: NF:ole2.OleQueryLinkFromData
title: OleQueryLinkFromData function (ole2.h)
description: Determines whether an OLE linked object (rather than an OLE embedded object) can be created from a clipboard data object.
helpviewer_keywords: ["OleQueryLinkFromData","OleQueryLinkFromData function [COM]","_ole_OleQueryLinkFromData","com.olequerylinkfromdata","ole2/OleQueryLinkFromData"]
old-location: com\olequerylinkfromdata.htm
tech.root: com
ms.assetid: 9ebdcd7f-06c1-4464-a66c-4d134a6b5d36
ms.date: 12/05/2018
ms.keywords: OleQueryLinkFromData, OleQueryLinkFromData function [COM], _ole_OleQueryLinkFromData, com.olequerylinkfromdata, ole2/OleQueryLinkFromData
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
 - OleQueryLinkFromData
 - ole2/OleQueryLinkFromData
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
 - OleQueryLinkFromData
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleQueryLinkFromData function


## -description

Determines whether an OLE linked object (rather than an OLE embedded object) can be created from a clipboard data object.

## -parameters

### -param pSrcDataObject [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the clipboard data object from which the object is to be created.

## -returns

Returns S_OK if the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkfromdata">OleCreateLinkFromData</a> function can be used to create the linked object; otherwise S_FALSE.

## -remarks

The <b>OleQueryLinkFromData</b> function is similar to the <a href="/windows/desktop/api/ole2/nf-ole2-olequerycreatefromdata">OleQueryCreateFromData</a> function, but determines whether an OLE linked object (rather than an OLE embedded object) can be created from the clipboard data object. If the return value is S_OK, the application can then attempt to create the object with a call to <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkfromdata">OleCreateLinkFromData</a>. A successful return from <b>OleQueryLinkFromData</b> does not, however, guarantee the successful creation of a link.
