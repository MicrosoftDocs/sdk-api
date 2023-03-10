---
UID: NF:objidlbase.IMarshal.ReleaseMarshalData
title: IMarshal::ReleaseMarshalData (objidlbase.h)
description: The IMarshal::ReleaseMarshalData (objidlbase.h) method destroys a marshaled data packet.
helpviewer_keywords: ["IMarshal interface [COM]","ReleaseMarshalData method","IMarshal.ReleaseMarshalData","IMarshal::ReleaseMarshalData","ReleaseMarshalData","ReleaseMarshalData method [COM]","ReleaseMarshalData method [COM]","IMarshal interface","_com_imarshal_releasemarshaldata","com.imarshal_releasemarshaldata","objidlbase/IMarshal::ReleaseMarshalData"]
old-location: com\imarshal_releasemarshaldata.htm
tech.root: com
ms.assetid: c58c7768-9200-4370-930c-89a6c6d2b430
ms.date: 08/13/2022
ms.keywords: IMarshal interface [COM],ReleaseMarshalData method, IMarshal.ReleaseMarshalData, IMarshal::ReleaseMarshalData, ReleaseMarshalData, ReleaseMarshalData method [COM], ReleaseMarshalData method [COM],IMarshal interface, _com_imarshal_releasemarshaldata, com.imarshal_releasemarshaldata, objidlbase/IMarshal::ReleaseMarshalData
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IMarshal::ReleaseMarshalData
 - objidlbase/IMarshal::ReleaseMarshalData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IMarshal.ReleaseMarshalData
---

# IMarshal::ReleaseMarshalData


## -description

Destroys a marshaled data packet.

## -parameters

### -param pStm [in]

A pointer to a stream that contains the data packet to be destroyed.

## -returns

This method can return the standard return values S_OK and E_FAIL, as well as any of the stream-access errors for the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface.

## -remarks

If an object's marshaled data packet does not get unmarshaled in the client process space and the packet is no longer needed, the client calls <b>ReleaseMarshalData</b> on the proxy's <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> implementation to instruct the object to destroy the data packet. The call occurs within the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a> function. The data packet serves as an additional reference on the object, and releasing the data is like releasing an interface pointer by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.

If the marshaled data packet somehow does not arrive in the client process or if <b>ReleaseMarshalData</b> is not successfully re-created in the proxy, COM can call this method on the object itself.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You will rarely if ever have occasion to call this method yourself. A possible exception would be if you were to implement <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> on a class factory for a class object on which you are also implementing <b>IMarshal</b>. In this case, if you were marshaling the object to a table where it could be retrieved by multiple clients, you might, as part of your unmarshaling routine, call <b>ReleaseMarshalData</b> to release the data packet for each proxy.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If your implementation stores state information about marshaled data packets, you can use this method to release the state information associated with the data packet represented by <i>pStm</i>. Your implementation should also position the seek pointer in the stream past the last byte of data.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>
