---
UID: NN:mfobjects.IMFByteStreamProxyClassFactory
title: IMFByteStreamProxyClassFactory
author: windows-sdk-content
description: Creates a proxy to a byte stream.
old-location: mf\imfbytestreamproxyclassfactory.htm
tech.root: medfound
ms.assetid: DF29B5FC-864F-4400-8EDB-3A2CD797E37A
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFByteStreamProxyClassFactory, IMFByteStreamProxyClassFactory interface [Media Foundation], IMFByteStreamProxyClassFactory interface [Media Foundation],described, mf.imfbytestreamproxyclassfactory, mfobjects/IMFByteStreamProxyClassFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamProxyClassFactory interface


## -description


Creates a proxy to a byte stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamProxyClassFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFByteStreamProxyClassFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5A7E6218-615F-43E3-BB96-0D39138A4E28">CreateByteStreamProxy</a>
</td>
<td align="left" width="63%">
Creates a proxy to a byte stream.

</td>
</tr>
</table> 


## -remarks



This interface provides a factory object for creating a proxy to an existing Microsoft Media Foundation byte stream. The CLSID of the factory object is <b>CLSID_MFByteStreamProxyClassFactory</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

