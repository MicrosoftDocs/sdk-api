---
UID: NF:callobj.ICallFrame.ReleaseMarshalData
title: ICallFrame::ReleaseMarshalData (callobj.h)
description: Releases resources that are held by interface pointers residing in a packet of marshaled data. This method finds all interface pointers in the packet, and calls the CoReleaseMarshalData function on each one.
helpviewer_keywords: ["ICallFrame interface [COM]","ReleaseMarshalData method","ICallFrame.ReleaseMarshalData","ICallFrame::ReleaseMarshalData","ReleaseMarshalData","ReleaseMarshalData method [COM]","ReleaseMarshalData method [COM]","ICallFrame interface","_com_icallframe_releasemarshaldata","callobj/ICallFrame::ReleaseMarshalData","com.icallframe_releasemarshaldata"]
old-location: com\icallframe_releasemarshaldata.htm
tech.root: com
ms.assetid: c82107ad-68d1-4a46-ba78-37592d445c57
ms.date: 12/05/2018
ms.keywords: ICallFrame interface [COM],ReleaseMarshalData method, ICallFrame.ReleaseMarshalData, ICallFrame::ReleaseMarshalData, ReleaseMarshalData, ReleaseMarshalData method [COM], ReleaseMarshalData method [COM],ICallFrame interface, _com_icallframe_releasemarshaldata, callobj/ICallFrame::ReleaseMarshalData, com.icallframe_releasemarshaldata
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
 - ICallFrame::ReleaseMarshalData
 - callobj/ICallFrame::ReleaseMarshalData
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
 - ICallFrame.ReleaseMarshalData
---

# ICallFrame::ReleaseMarshalData


## -description

Releases resources that are held by interface pointers residing in a packet of marshaled data. This method finds all interface pointers in the packet, and calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a> function on each one.

## -parameters

### -param pBuffer [in]

A pointer to the buffer containing the marshaled [out] values.

### -param cbBuffer [in]

The size of the buffer, in bytes.

### -param ibFirstRelease [in]

The first byte in the buffer, which is to be released. A value of zero implies that the interface pointers in the whole buffer are to be released. The marshaled interface pointers are assumed to have been released by some other mechanism.

### -param dataRep [in]

The data representation with which the data was marshaled.

### -param pcontext [in]

A pointer to the <a href="/windows/win32/api/callobj/ns-callobj-callframe_marshalcontext">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how un-marshalling is carried out.

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

The <b>ReleaseMarshalData</b> method must be called exactly once to clean up the resources held in a marshaled buffer. However when the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshlflags">MSHLFLAGS</a> enumeration is set to MSHLFLAGS_NORMAL, this is done automatically during un-marshaling and so need not be carried out explicitly.

This method can function correctly on both marshaled [in] and [out] parameters.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>