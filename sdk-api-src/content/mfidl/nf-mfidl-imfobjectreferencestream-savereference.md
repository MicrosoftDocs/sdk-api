---
UID: NF:mfidl.IMFObjectReferenceStream.SaveReference
title: IMFObjectReferenceStream::SaveReference (mfidl.h)
description: Stores the data needed to marshal an interface across a process boundary.
helpviewer_keywords: ["776f94c4-d0e9-4fb7-a39c-32c83428bbe3","IMFObjectReferenceStream interface [Media Foundation]","SaveReference method","IMFObjectReferenceStream.SaveReference","IMFObjectReferenceStream::SaveReference","SaveReference","SaveReference method [Media Foundation]","SaveReference method [Media Foundation]","IMFObjectReferenceStream interface","mf.imfobjectreferencestream_savereference","mfidl/IMFObjectReferenceStream::SaveReference"]
old-location: mf\imfobjectreferencestream_savereference.htm
tech.root: mf
ms.assetid: 776f94c4-d0e9-4fb7-a39c-32c83428bbe3
ms.date: 12/05/2018
ms.keywords: 776f94c4-d0e9-4fb7-a39c-32c83428bbe3, IMFObjectReferenceStream interface [Media Foundation],SaveReference method, IMFObjectReferenceStream.SaveReference, IMFObjectReferenceStream::SaveReference, SaveReference, SaveReference method [Media Foundation], SaveReference method [Media Foundation],IMFObjectReferenceStream interface, mf.imfobjectreferencestream_savereference, mfidl/IMFObjectReferenceStream::SaveReference
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFObjectReferenceStream::SaveReference
 - mfidl/IMFObjectReferenceStream::SaveReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFObjectReferenceStream.SaveReference
---

# IMFObjectReferenceStream::SaveReference


## -description

Stores the data needed to marshal an interface across a process boundary.

## -parameters

### -param riid [in]

Interface identifier of the interface to marshal.

### -param pUnk [in]

Pointer to the <b>IUnknown</b> interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream">IMFObjectReferenceStream</a>