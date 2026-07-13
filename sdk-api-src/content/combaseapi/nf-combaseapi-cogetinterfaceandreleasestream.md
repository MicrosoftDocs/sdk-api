---
UID: NF:combaseapi.CoGetInterfaceAndReleaseStream
title: CoGetInterfaceAndReleaseStream function (combaseapi.h)
description: Unmarshals a buffer containing an interface pointer and releases the stream when an interface pointer has been marshaled from another thread to the calling thread.
helpviewer_keywords: ["CoGetInterfaceAndReleaseStream","CoGetInterfaceAndReleaseStream function [COM]","_com_CoGetInterfaceAndReleaseStream","com.cogetinterfaceandreleasestream","combaseapi/CoGetInterfaceAndReleaseStream"]
old-location: com\cogetinterfaceandreleasestream.htm
tech.root: com
ms.assetid: b529f65f-3208-4594-a772-d1cad3727dc1
ms.date: 12/05/2018
ms.keywords: CoGetInterfaceAndReleaseStream, CoGetInterfaceAndReleaseStream function [COM], _com_CoGetInterfaceAndReleaseStream, com.cogetinterfaceandreleasestream, combaseapi/CoGetInterfaceAndReleaseStream
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
 - CoGetInterfaceAndReleaseStream
 - combaseapi/CoGetInterfaceAndReleaseStream
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
 - CoGetInterfaceAndReleaseStream
---

# CoGetInterfaceAndReleaseStream function


## -description

Unmarshals a buffer containing an interface pointer and releases the stream when an interface pointer has been marshaled from another thread to the calling thread.

## -parameters

### -param pStm [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface on the stream to be unmarshaled.

### -param iid [in]

A reference to the identifier of the interface requested from the unmarshaled object.

### -param ppv [out]

The address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppv</i> contains the requested interface pointer to the unmarshaled interface.

## -returns

This function can return the standard return values S_OK and E_INVALIDARG, as well as any of the values returned by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>.

## -remarks

<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data.

</div>
<div> </div>
The <b>CoGetInterfaceAndReleaseStream</b> function performs the following tasks: 

<ul>
<li>Calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a> to unmarshal an interface pointer previously passed in a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream">CoMarshalInterThreadInterfaceInStream</a>.
</li>
<li>Releases the stream pointer. Even if the unmarshaling fails, the stream is still released because there is no effective way to recover from a failure of this kind.
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream">CoMarshalInterThreadInterfaceInStream</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>