---
UID: NN:wmsdkidl.IWMSyncReader2
title: IWMSyncReader2 (wmsdkidl.h)
description: The IWMSyncReader2 interface provides advanced features for the synchronous reader.
helpviewer_keywords: ["IWMSyncReader2","IWMSyncReader2 interface [windows Media Format]","IWMSyncReader2 interface [windows Media Format]","described","IWMSyncReader2Interface","wmformat.iwmsyncreader2","wmsdkidl/IWMSyncReader2"]
old-location: wmformat\iwmsyncreader2.htm
tech.root: wmformat
ms.assetid: f3db7530-a662-46f1-bc64-1dd4523dc87c
ms.date: 12/05/2018
ms.keywords: IWMSyncReader2, IWMSyncReader2 interface [windows Media Format], IWMSyncReader2 interface [windows Media Format],described, IWMSyncReader2Interface, wmformat.iwmsyncreader2, wmsdkidl/IWMSyncReader2
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
 - IWMSyncReader2
 - wmsdkidl/IWMSyncReader2
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
 - IWMSyncReader2
---

# IWMSyncReader2 interface


## -description

The <b>IWMSyncReader2</b> interface provides advanced features for the synchronous reader. It contains methods for allocating samples manually and for seeking to SMPTE time codes.

An <b>IWMSyncReader2</b> interface exists for every synchronous reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the synchronous reader object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSyncReader2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader</a>. <b>IWMSyncReader2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
