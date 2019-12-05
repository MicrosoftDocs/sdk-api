---
UID: NN:mfobjects.IMFByteStreamProxyClassFactory
title: IMFByteStreamProxyClassFactory (mfobjects.h)
description: Creates a proxy to a byte stream.
old-location: mf\imfbytestreamproxyclassfactory.htm
tech.root: medfound
ms.assetid: DF29B5FC-864F-4400-8EDB-3A2CD797E37A
ms.date: 12/05/2018
ms.keywords: IMFByteStreamProxyClassFactory, IMFByteStreamProxyClassFactory interface [Media Foundation], IMFByteStreamProxyClassFactory interface [Media Foundation],described, mf.imfbytestreamproxyclassfactory, mfobjects/IMFByteStreamProxyClassFactory
ms.topic: interface
f1_keywords:
- mfobjects/IMFByteStreamProxyClassFactory
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfobjects.h
api_name:
- IMFByteStreamProxyClassFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStreamProxyClassFactory interface


## -description


Creates a proxy to a byte stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamProxyClassFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamProxyClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamProxyClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestreamproxyclassfactory-createbytestreamproxy">CreateByteStreamProxy</a>
</td>
<td align="left" width="63%">
Creates a proxy to a byte stream.

</td>
</tr>
</table> 


## -remarks



This interface provides a factory object for creating a proxy to an existing Microsoft Media Foundation byte stream. The CLSID of the factory object is <b>CLSID_MFByteStreamProxyClassFactory</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

