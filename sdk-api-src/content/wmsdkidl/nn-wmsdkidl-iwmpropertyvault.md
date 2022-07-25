---
UID: NN:wmsdkidl.IWMPropertyVault
title: IWMPropertyVault (wmsdkidl.h)
description: The IWMPropertyVault interface provides methods to store and retrieve properties.
helpviewer_keywords: ["IWMPropertyVault","IWMPropertyVault interface [windows Media Format]","IWMPropertyVault interface [windows Media Format]","described","IWMPropertyVaultInterface","wmformat.iwmpropertyvault","wmsdkidl/IWMPropertyVault"]
old-location: wmformat\iwmpropertyvault.htm
tech.root: wmformat
ms.assetid: 0e51a9be-afd4-430b-8339-f45e8f9a7d20
ms.date: 12/05/2018
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

The <b>IWMPropertyVault</b> interface provides methods to store and retrieve properties. Currently, you can use this interface to set properties associated with variable bit rate (VBR) encoding. The generic nature of <b>IWMPropertyVault</b> allows for its use in other situations in future versions of the Format SDK.

<b>IWMPropertyVault</b> is exposed by stream configuration objects. To obtain a pointer to <b>IWMPropertyVault</b>, you must call the <b>QueryInterface</b> method of one of the other interfaces of an existing stream configuration object.

## -inheritance

The <b>IWMPropertyVault</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPropertyVault</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/stream-configuration-object">Stream Configuration Object</a>
