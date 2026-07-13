---
UID: NN:wmsdkidl.IWMPropertyVault
title: IWMPropertyVault (wmsdkidl.h)
description: The IWMPropertyVault interface provides methods to store and retrieve properties.
helpviewer_keywords: ["IWMPropertyVault","IWMPropertyVault interface [windows Media Format]","IWMPropertyVault interface [windows Media Format]","described","IWMPropertyVaultInterface","wmformat.iwmpropertyvault","wmsdkidl/IWMPropertyVault"]
old-location: wmformat\iwmpropertyvault.htm
tech.root: wmformat
ms.assetid: 0e51a9be-afd4-430b-8339-f45e8f9a7d20
ms.date: 4/26/2023
ms.keywords: IWMPropertyVault, IWMPropertyVault interface [windows Media Format], IWMPropertyVault interface [windows Media Format],described, IWMPropertyVaultInterface, wmformat.iwmpropertyvault, wmsdkidl/IWMPropertyVault
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
 - IWMPropertyVault
 - wmsdkidl/IWMPropertyVault
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
 - IWMPropertyVault
---

# IWMPropertyVault interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPropertyVault</b> interface provides methods to store and retrieve properties. Currently, you can use this interface to set properties associated with variable bit rate (VBR) encoding. The generic nature of <b>IWMPropertyVault</b> allows for its use in other situations in future versions of the Format SDK.

<b>IWMPropertyVault</b> is exposed by stream configuration objects. To obtain a pointer to <b>IWMPropertyVault</b>, you must call the <b>QueryInterface</b> method of one of the other interfaces of an existing stream configuration object.

## -inheritance

The <b>IWMPropertyVault</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPropertyVault</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/stream-configuration-object">Stream Configuration Object</a>
