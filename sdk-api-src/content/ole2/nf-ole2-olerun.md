---
UID: NF:ole2.OleRun
title: OleRun function (ole2.h)
description: Puts an OLE compound document object into the running state.
helpviewer_keywords: ["OleRun","OleRun function [COM]","_ole_OleRun","com.olerun","ole2/OleRun"]
old-location: com\olerun.htm
tech.root: com
ms.assetid: 9035f996-b163-4855-aa9d-184b77072ead
ms.date: 12/05/2018
ms.keywords: OleRun, OleRun function [COM], _ole_OleRun, com.olerun, ole2/OleRun
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
 - OleRun
 - ole2/OleRun
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
 - API-MS-Win-OLE32-IE-l1-1-0.dll
 - ole32_wp.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleRun
req.apiset: ext-ms-win-com-ole32-l1-1-1 (introduced in Windows 8.1)
---

# OleRun function


## -description

Puts an OLE compound document object into the running state.

## -parameters

### -param pUnknown [in]

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the object, with which it will query for a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a> interface, and then call its <a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-run">Run</a> method.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CLASSDIFF</b></dt>
</dl>
</td>
<td width="60%">
The source of an OLE link has been converted to a different class.

</td>
</tr>
</table>

## -remarks

The <b>OleRun</b> function puts an object in the running state. The implementation of <b>OleRun</b> was changed in OLE 2.01 to coincide with the publication of the <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a> interface. You can use <b>OleRun</b> and <a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-run">IRunnableObject::Run</a> interchangeably. <b>OleRun</b> queries the object for a pointer to <b>IRunnableObject</b>. If successful, the function returns the results of calling the <b>IRunnableObject::Run</b> method.

For more information on using this function, see <a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-run">IRunnableObject::Run</a>.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a>



<a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-run">IRunnableObject::Run</a>
