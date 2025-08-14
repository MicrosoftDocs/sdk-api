---
UID: NF:combaseapi.CoMarshalInterThreadInterfaceInStream
title: CoMarshalInterThreadInterfaceInStream function (combaseapi.h)
description: Marshals an interface pointer from one thread to another thread in the same process.
helpviewer_keywords: ["CoMarshalInterThreadInterfaceInStream","CoMarshalInterThreadInterfaceInStream function [COM]","_com_CoMarshalInterThreadInterfaceInStream","com.comarshalinterthreadinterfaceinstream","combaseapi/CoMarshalInterThreadInterfaceInStream"]
old-location: com\comarshalinterthreadinterfaceinstream.htm
tech.root: com
ms.assetid: c9ab8713-8604-4f0b-a11b-bdfb7d595d95
ms.date: 12/05/2018
ms.keywords: CoMarshalInterThreadInterfaceInStream, CoMarshalInterThreadInterfaceInStream function [COM], _com_CoMarshalInterThreadInterfaceInStream, com.comarshalinterthreadinterfaceinstream, combaseapi/CoMarshalInterThreadInterfaceInStream
req.header: combaseapi.h
req.include-header: Objbase.h
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
 - CoMarshalInterThreadInterfaceInStream
 - combaseapi/CoMarshalInterThreadInterfaceInStream
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
 - CoMarshalInterThreadInterfaceInStream
---

# CoMarshalInterThreadInterfaceInStream function


## -description

Marshals an interface pointer from one thread to another thread in the same process.

## -parameters

### -param riid [in]

A reference to the identifier of the interface to be marshaled.

### -param pUnk [in]

A pointer to the interface to be marshaled, which must be derived from <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. This parameter can be <b>NULL</b>.

### -param ppStm [out]

The address of the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>* pointer variable that receives the interface pointer to the stream that contains the marshaled interface.

## -returns

This function can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

The <b>CoMarshalInterThreadInterfaceInStream</b> function enables an object to easily and reliably marshal an interface pointer to another thread in the same process. The stream returned in the <i>ppStm</i> parameter is guaranteed to behave correctly when a client running in the receiving thread attempts to unmarshal the pointer. The client can then call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream">CoGetInterfaceAndReleaseStream</a> to unmarshal the interface pointer and release the stream object.

The <b>CoMarshalInterThreadInterfaceInStream</b> function performs the following tasks:

<ol>
<li>
Creates a stream object.

</li>
<li>
Passes the stream object's IStream pointer to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>.

</li>
<li>
Returns the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer to the caller.

</li>
</ol>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream">CoGetInterfaceAndReleaseStream</a>