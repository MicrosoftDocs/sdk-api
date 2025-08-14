---
UID: NF:objbase.CreateItemMoniker
title: CreateItemMoniker function (objbase.h)
description: Creates an item moniker that identifies an object within a containing object (typically a compound document).
helpviewer_keywords: ["CreateItemMoniker","CreateItemMoniker function [COM]","_com_CreateItemMoniker","com.createitemmoniker","objbase/CreateItemMoniker"]
old-location: com\createitemmoniker.htm
tech.root: com
ms.assetid: 339919ed-660c-4239-825b-7fa96c48e5cd
ms.date: 12/05/2018
ms.keywords: CreateItemMoniker, CreateItemMoniker function [COM], _com_CreateItemMoniker, com.createitemmoniker, objbase/CreateItemMoniker
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - CreateItemMoniker
 - objbase/CreateItemMoniker
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
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CreateItemMoniker
req.apiset: ext-ms-win-com-ole32-l1-1-0 (introduced in Windows 8)
---

# CreateItemMoniker function


## -description

Creates an item moniker that identifies an object within a containing object (typically a compound document).

## -parameters

### -param lpszDelim [in]

A pointer to a wide character string (two bytes per character) zero-terminated string containing the delimiter (typically "!") used to separate this item's display name from the display name of its containing object.

### -param lpszItem [in]

A pointer to a zero-terminated string indicating the containing object's name for the object being identified. This name can later be used to retrieve a pointer to the object in a call to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a>.

### -param ppmk [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the item moniker. When successful, the function has called <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the item moniker and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, the supplied interface pointer has a <b>NULL</b> value.

## -returns

This function can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

A moniker provider, which hands out monikers to identify its objects so they are accessible to other parties, would call <b>CreateItemMoniker</b> to identify its objects with item monikers. Item monikers are based on a string, and identify objects that are contained within another object and can be individually identified using a string. The containing object must also implement the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolecontainer">IOleContainer</a> interface. 

Most moniker providers are OLE applications that support linking. Applications that support linking to objects smaller than file-based documents, such as a server application that allows linking to a selection within a document, should use item monikers to identify the objects. Container applications that allow linking to embedded objects use item monikers to identify the embedded objects. 



The <i>lpszItem</i> parameter is the name used by the document to uniquely identify the object. For example, if the object being identified is a cell range in a spreadsheet, an appropriate name might be something like "A1:E7." An appropriate name when the object being identified is an embedded object might be something like "embedobj1." The containing object must provide an implementation of the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface that can interpret this name and locate the corresponding object. This allows the item moniker to be bound to the object it identifies.

Item monikers are not used in isolation. They must be composed with a moniker that identifies the containing object as well. For example, if the object being identified is a cell range contained in a file-based document, the item moniker identifying that object must be composed with the file moniker identifying that document, resulting in a composite moniker that is the equivalent of "C:\work\sales.xls!A1:E7."

Nested containers are allowed also, as in the case where an object is contained within an embedded object inside another document. The complete moniker of such an object would be the equivalent of "C:\work\report.doc!embedobj1!A1:E7." In this case, each containing object must call <b>CreateItemMoniker</b> and provide its own implementation of the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-composewith">IMoniker::ComposeWith</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecontainer">IOleContainer</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>
