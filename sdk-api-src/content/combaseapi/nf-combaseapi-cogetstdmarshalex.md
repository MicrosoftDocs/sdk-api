---
UID: NF:combaseapi.CoGetStdMarshalEx
title: CoGetStdMarshalEx function (combaseapi.h)
description: Creates an aggregated standard marshaler for use with lightweight client-side handlers.
helpviewer_keywords: ["CoGetStdMarshalEx","CoGetStdMarshalEx function [COM]","SMEXF_HANDLER","SMEXF_SERVER","_com_CoGetStdMarshalEx","com.cogetstdmarshalex","combaseapi/CoGetStdMarshalEx"]
old-location: com\cogetstdmarshalex.htm
tech.root: com
ms.assetid: 405c5ff3-8702-48b3-9be9-df4a9461696e
ms.date: 12/05/2018
ms.keywords: CoGetStdMarshalEx, CoGetStdMarshalEx function [COM], SMEXF_HANDLER, SMEXF_SERVER, _com_CoGetStdMarshalEx, com.cogetstdmarshalex, combaseapi/CoGetStdMarshalEx
req.header: combaseapi.h
req.include-header: Objbase.h
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
 - CoGetStdMarshalEx
 - combaseapi/CoGetStdMarshalEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetStdMarshalEx
---

# CoGetStdMarshalEx function


## -description

Creates an aggregated standard marshaler for use with lightweight client-side handlers.

## -parameters

### -param pUnkOuter [in]

A pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>.

### -param smexflags [in]

One of two values indicating whether the aggregated standard marshaler is on the client side or the server side. These flags are defined in the <b>STDMSHLFLAGS</b> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMEXF_SERVER"></a><a id="smexf_server"></a><dl>
<dt><b>SMEXF_SERVER</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Indicates a server-side aggregated standard marshaler.

</td>
</tr>
<tr>
<td width="40%"><a id="SMEXF_HANDLER"></a><a id="smexf_handler"></a><dl>
<dt><b>SMEXF_HANDLER</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Indicates a client-side (handler) aggregated standard marshaler.

</td>
</tr>
</table>

### -param ppUnkInner [out]

On successful return, address of pointer to the <a href="/windows/desktop/com/iunknown-and-interface-inheritance">IUnknown</a> interface on the newly-created aggregated standard marshaler. If an error occurs, this value is <b>NULL</b>.

## -returns

This function returns S_OK.

## -remarks

The server calls <b>CoGetStdMarshalEx</b> passing in the flag SMEXF_SERVER. This creates a server side standard marshaler (known as a stub manager). The handler calls <b>CoGetStdMarshalEx</b> passing in the flag SMEXF_HANDLER. This creates a client side standard marshaler (known as a proxy manager). Note that when calling this function, the handler must pass the original controlling unknown that was passed to the handler when the handler was created. This will be the system implemented controlling unknown. Failure to pass the correct <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> results in an error returned. On success, the ppUnkInner returned is the controlling unknown of the inner object. The server and handler must keep this pointer, and may use it to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> for the <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> interface.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istdmarshalinfo">IStdMarshalInfo</a>



<a href="/windows/desktop/com/the-lightweight-client-side-handler">The Lightweight Client-Side Handler</a>