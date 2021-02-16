---
UID: NF:callobj.ICallFrame.Marshal
title: ICallFrame::Marshal (callobj.h)
description: Marshals the call frame by turning its reachable data into a flat buffer without disturbing the frame.
helpviewer_keywords: ["ICallFrame interface [COM]","Marshal method","ICallFrame.Marshal","ICallFrame::Marshal","Marshal","Marshal method [COM]","Marshal method [COM]","ICallFrame interface","_com_icallframe_marshal","callobj/ICallFrame::Marshal","com.icallframe_marshal"]
old-location: com\icallframe_marshal.htm
tech.root: com
ms.assetid: cab40c31-1f89-4da9-a1e0-ef946b34665c
ms.date: 12/05/2018
ms.keywords: ICallFrame interface [COM],Marshal method, ICallFrame.Marshal, ICallFrame::Marshal, Marshal, Marshal method [COM], Marshal method [COM],ICallFrame interface, _com_icallframe_marshal, callobj/ICallFrame::Marshal, com.icallframe_marshal
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
 - ICallFrame::Marshal
 - callobj/ICallFrame::Marshal
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
 - ICallFrame.Marshal
---

# ICallFrame::Marshal


## -description

Marshals the call frame by turning its reachable data into a flat buffer without disturbing the frame.

## -parameters

### -param pmshlContext [in]

A pointer to the <a href="/windows/win32/api/callobj/ns-callobj-callframe_marshalcontext">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how marshalling is carried out.

### -param mshlflags [in]

Flag indicating whether the data to be marshaled is to be transmitted back to the client process - the normal case - or written to a global table, where it can be retrieved by multiple clients. The possible values are from the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshlflags">MSHLFLAGS</a> enumeration.

### -param pBuffer [in]

A pointer to the buffer into which the marshaled data is to be placed.

### -param cbBuffer [in]

The size of the buffer, in bytes.

### -param pcbBufferUsed [out]

Receives the size of the buffer that was actually used. This parameter is optional.

### -param pdataRep [out]

Receives the NDR data representation with which the data was marshaled. This parameter is optional. For more information, see <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getbuffer">IRpcChannelBuffer::GetBuffer</a>.

### -param prpcFlags [out]

Receives an RPC flag associated with the call. This parameter is optional. For more information, see <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getbuffer">IRpcChannelBuffer::GetBuffer</a>.

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

When marshalling the [In] versions of [in, out] parameters are present, and the [out] versions are undefined. When marshalling [out] parameters the values are valid.

If this method returns an error, the caller will not be able to clean it up. Resources such as memory transiently allocated during the attempted marshalling have been freed.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>