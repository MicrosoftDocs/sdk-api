---
UID: NF:callobj.ICallUnmarshal.ReleaseMarshalData
title: ICallUnmarshal::ReleaseMarshalData (callobj.h)
description: Releases resources that may be held by interface pointers residing in a packet of marshaled data. This method finds all interface pointers in the packet and calls the CoReleaseMarshalData function on each interface pointer.
helpviewer_keywords: ["ICallUnmarshal interface [COM]","ReleaseMarshalData method","ICallUnmarshal.ReleaseMarshalData","ICallUnmarshal::ReleaseMarshalData","ReleaseMarshalData","ReleaseMarshalData method [COM]","ReleaseMarshalData method [COM]","ICallUnmarshal interface","_com_icallunmarshal_releasemarshaldata","callobj/ICallUnmarshal::ReleaseMarshalData","com.icallunmarshal_releasemarshaldata"]
old-location: com\icallunmarshal_releasemarshaldata.htm
tech.root: com
ms.assetid: c7b1aff8-338a-491a-908f-5f85dddd89b7
ms.date: 12/05/2018
ms.keywords: ICallUnmarshal interface [COM],ReleaseMarshalData method, ICallUnmarshal.ReleaseMarshalData, ICallUnmarshal::ReleaseMarshalData, ReleaseMarshalData, ReleaseMarshalData method [COM], ReleaseMarshalData method [COM],ICallUnmarshal interface, _com_icallunmarshal_releasemarshaldata, callobj/ICallUnmarshal::ReleaseMarshalData, com.icallunmarshal_releasemarshaldata
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICallUnmarshal::ReleaseMarshalData
 - callobj/ICallUnmarshal::ReleaseMarshalData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallUnmarshal.ReleaseMarshalData
---

# ICallUnmarshal::ReleaseMarshalData


## -description

Releases resources that may be held by interface pointers residing in a packet of marshaled data. This method finds all interface pointers in the packet and calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a> function on each interface pointer.

## -parameters

### -param iMethod [in]

The method number.

### -param pBuffer [in]

A pointer to the buffer containing the marshaled out parameters.

### -param cbBuffer [in]

The size of the buffer, in bytes.

### -param ibFirstRelease [in]

The first byte in the buffer to be released. A value of zero implies that the interface pointers in the whole buffer are to be released. The idea is that marshaled interface pointers prior to the indicated byte are assumed to have already been released by some other mechanism.

### -param dataRep [in]

The data representation with which the data was marshaled.

### -param pcontext [in]

A pointer to a <a href="/windows/win32/api/callobj/ns-callobj-callframe_marshalcontext">CALLFRAME_MARSHALCONTEXT</a> structure that contains information about the context in which unmarshaling is to be carried out.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -remarks

To clean up resources held in the marshaled buffer, the <b>ReleaseMarshalData</b> method must be called. However when the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshlflags">MSHLFLAGS</a> enumeration is set to normal, this is done automatically when unmarshaling.

<b>ReleaseMarshalData</b> can be used on both marshaled in and out parameters.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallunmarshal">ICallUnmarshal</a>