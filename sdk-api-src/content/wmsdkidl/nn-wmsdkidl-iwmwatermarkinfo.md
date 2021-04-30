---
UID: NN:wmsdkidl.IWMWatermarkInfo
title: IWMWatermarkInfo (wmsdkidl.h)
description: The IWMWatermarkInfo interface retrieves information about available watermarking systems.
helpviewer_keywords: ["IWMWatermarkInfo","IWMWatermarkInfo interface [windows Media Format]","IWMWatermarkInfo interface [windows Media Format]","described","IWMWatermarkInfoInterface","wmformat.iwmwatermarkinfo","wmsdkidl/IWMWatermarkInfo"]
old-location: wmformat\iwmwatermarkinfo.htm
tech.root: wmformat
ms.assetid: 4bdad433-31d1-442c-9701-f3748245070d
ms.date: 12/05/2018
ms.keywords: IWMWatermarkInfo, IWMWatermarkInfo interface [windows Media Format], IWMWatermarkInfo interface [windows Media Format],described, IWMWatermarkInfoInterface, wmformat.iwmwatermarkinfo, wmsdkidl/IWMWatermarkInfo
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
 - IWMWatermarkInfo
 - wmsdkidl/IWMWatermarkInfo
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
 - IWMWatermarkInfo
---

# IWMWatermarkInfo interface


## -description

The <b>IWMWatermarkInfo</b> interface retrieves information about available watermarking systems. Watermarking systems are implemented in DirectX Media Objects that are registered for use with the Windows Media Formats SDK.

An <b>IWMWatermarkInfo</b> interface exists for every writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on any other interface of the writer object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWatermarkInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWatermarkInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/watermarking-support">Watermarking Support</a>
