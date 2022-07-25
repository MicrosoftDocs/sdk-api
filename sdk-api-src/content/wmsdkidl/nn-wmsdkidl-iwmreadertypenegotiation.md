---
UID: NN:wmsdkidl.IWMReaderTypeNegotiation
title: IWMReaderTypeNegotiation (wmsdkidl.h)
description: The IWMReaderTypeNegotiation interface provides a single method that can be used to test certain changes to the output properties of a stream.An IWMReaderTypeNegotiation interface exists for every reader object.
helpviewer_keywords: ["IWMReaderTypeNegotiation","IWMReaderTypeNegotiation interface [windows Media Format]","IWMReaderTypeNegotiation interface [windows Media Format]","described","IWMReaderTypeNegotiationInterface","wmformat.iwmreadertypenegotiation","wmsdkidl/IWMReaderTypeNegotiation"]
old-location: wmformat\iwmreadertypenegotiation.htm
tech.root: wmformat
ms.assetid: 289ca857-5421-47f8-927e-6ca4204a31f9
ms.date: 12/05/2018
ms.keywords: IWMReaderTypeNegotiation, IWMReaderTypeNegotiation interface [windows Media Format], IWMReaderTypeNegotiation interface [windows Media Format],described, IWMReaderTypeNegotiationInterface, wmformat.iwmreadertypenegotiation, wmsdkidl/IWMReaderTypeNegotiation
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IWMReaderTypeNegotiation
 - wmsdkidl/IWMReaderTypeNegotiation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMReaderTypeNegotiation
---

# IWMReaderTypeNegotiation interface


## -description

The <b>IWMReaderTypeNegotiation</b> interface provides a single method that can be used to test certain changes to the output properties of a stream.

An <b>IWMReaderTypeNegotiation</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b>IWMReaderTypeNegotiation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderTypeNegotiation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>
