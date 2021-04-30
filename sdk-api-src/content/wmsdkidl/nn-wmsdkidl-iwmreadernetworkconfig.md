---
UID: NN:wmsdkidl.IWMReaderNetworkConfig
title: IWMReaderNetworkConfig (wmsdkidl.h)
description: The IWMReaderNetworkConfig interface is used to set and test network configuration settings.
helpviewer_keywords: ["IWMReaderNetworkConfig","IWMReaderNetworkConfig interface [windows Media Format]","IWMReaderNetworkConfig interface [windows Media Format]","described","IWMReaderNetworkConfigInterface","wmformat.iwmreadernetworkconfig","wmsdkidl/IWMReaderNetworkConfig"]
old-location: wmformat\iwmreadernetworkconfig.htm
tech.root: wmformat
ms.assetid: 0957ece7-93fe-411b-b69e-fd03933b09d1
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], IWMReaderNetworkConfig interface [windows Media Format],described, IWMReaderNetworkConfigInterface, wmformat.iwmreadernetworkconfig, wmsdkidl/IWMReaderNetworkConfig
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
 - IWMReaderNetworkConfig
 - wmsdkidl/IWMReaderNetworkConfig
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
 - IWMReaderNetworkConfig
---

# IWMReaderNetworkConfig interface


## -description

The <b>IWMReaderNetworkConfig</b> interface is used to set and test network configuration settings. By using this interface, the application can configure which protocols must be used to receive the stream as well as other advanced network settings, such as proxy specification and buffering time.

An <b>IWMReaderNetworkConfig</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderNetworkConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderNetworkConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>
