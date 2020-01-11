---
UID: NF:mfidl.IMFNetProxyLocatorFactory.CreateProxyLocator
title: IMFNetProxyLocatorFactory::CreateProxyLocator (mfidl.h)
description: Creates an IMFNetProxyLocator interface proxy locator object based on the protocol name.
old-location: mf\imfnetproxylocatorfactory_createproxylocator.htm
tech.root: medfound
ms.assetid: 0bdc03a8-a01d-453b-92b9-b39d8028b314
ms.date: 12/05/2018
ms.keywords: 0bdc03a8-a01d-453b-92b9-b39d8028b314, CreateProxyLocator, CreateProxyLocator method [Media Foundation], CreateProxyLocator method [Media Foundation],IMFNetProxyLocatorFactory interface, IMFNetProxyLocatorFactory interface [Media Foundation],CreateProxyLocator method, IMFNetProxyLocatorFactory.CreateProxyLocator, IMFNetProxyLocatorFactory::CreateProxyLocator, mf.imfnetproxylocatorfactory_createproxylocator, mfidl/IMFNetProxyLocatorFactory::CreateProxyLocator
f1_keywords:
- mfidl/IMFNetProxyLocatorFactory.CreateProxyLocator
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFNetProxyLocatorFactory.CreateProxyLocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetProxyLocatorFactory::CreateProxyLocator


## -description



Creates an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator">IMFNetProxyLocator</a> interface proxy locator object based on the protocol name.




## -parameters




### -param pszProtocol [in]

Null-terminated wide-character string containing the protocol name (for example, RTSP or HTTP).


### -param ppProxyLocator [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator">IMFNetProxyLocator</a> interface. The caller must release the interface.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory">IMFNetProxyLocatorFactory</a>
 

 

