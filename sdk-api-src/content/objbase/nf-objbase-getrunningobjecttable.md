---
UID: NF:objbase.GetRunningObjectTable
title: GetRunningObjectTable function (objbase.h)
description: Returns a pointer to the IRunningObjectTable interface on the local running object table (ROT).
helpviewer_keywords: ["GetRunningObjectTable","GetRunningObjectTable function [COM]","_com_GetRunningObjectTable","com.getrunningobjecttable","objbase/GetRunningObjectTable"]
old-location: com\getrunningobjecttable.htm
tech.root: com
ms.assetid: 65d9cf7d-cc8a-4199-9a4a-7fd67ef8872d
ms.date: 12/05/2018
ms.keywords: GetRunningObjectTable, GetRunningObjectTable function [COM], _com_GetRunningObjectTable, com.getrunningobjecttable, objbase/GetRunningObjectTable
req.header: objbase.h
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
 - GetRunningObjectTable
 - objbase/GetRunningObjectTable
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
 - GetRunningObjectTable
req.apiset: ext-ms-win-com-ole32-l1-1-0 (introduced in Windows 8)
---

# GetRunningObjectTable function


## -description

Returns a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a> interface on the local running object table (ROT).

## -parameters

### -param reserved [in]

This parameter is reserved and must be 0.

### -param pprot [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>* pointer variable that receives the interface pointer to the local ROT. When the function is successful, the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the interface pointer. If an error occurs, *<i>pprot</i> is undefined.

## -returns

This function can return the standard return values E_UNEXPECTED and S_OK.

## -remarks

Each workstation has a local ROT that maintains a table of the objects that have been registered as running on that computer. This function returns an <a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a> interface pointer, which provides access to that table.

Moniker providers, which hand out monikers that identify objects so they are accessible to others, should call <b>GetRunningObjectTable</b>. Use the interface pointer returned by this function to register your objects when they begin running, to record the times that those objects are modified, and to revoke their registrations when they stop running. See the <a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a> interface for more information.



Compound-document link sources are the most common example of moniker providers. These include server applications that support linking to their documents (or portions of a document) and container applications that support linking to embeddings within their documents. Server applications that do not support linking can also use the ROT to cooperate with container applications that support linking to embeddings.

If you are implementing the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface to write a new moniker class, and you need an interface pointer to the ROT, call <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a> rather than the <b>GetRunningObjectTable</b> function. This allows future implementations of the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface to modify binding behavior.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>
