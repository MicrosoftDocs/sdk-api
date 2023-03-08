---
UID: NN:wmsinternaladminnetsource.IWMSInternalAdminNetSource2
title: IWMSInternalAdminNetSource2 (wmsinternaladminnetsource.h)
description: The IWMSInternalAdminNetSource2 interface provides improved methods for password caching.
helpviewer_keywords: ["IWMSInternalAdminNetSource2","IWMSInternalAdminNetSource2 interface [windows Media Format]","IWMSInternalAdminNetSource2 interface [windows Media Format]","described","IWMSInternalAdminNetSource2Interface","wmformat.iwmsinternaladminnetsource2","wmsinternaladminnetsource/IWMSInternalAdminNetSource2"]
old-location: wmformat\iwmsinternaladminnetsource2.htm
tech.root: wmformat
ms.assetid: 6d334725-11d5-4249-a83d-fc8c1c35a56f
ms.date: 12/05/2018
ms.keywords: IWMSInternalAdminNetSource2, IWMSInternalAdminNetSource2 interface [windows Media Format], IWMSInternalAdminNetSource2 interface [windows Media Format],described, IWMSInternalAdminNetSource2Interface, wmformat.iwmsinternaladminnetsource2, wmsinternaladminnetsource/IWMSInternalAdminNetSource2
req.header: wmsinternaladminnetsource.h
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
 - IWMSInternalAdminNetSource2
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsinternaladminnetsource.h
api_name:
 - IWMSInternalAdminNetSource2
 - IWMSInternalAdminNetSource2.FindProxyForURLEx
---

# IWMSInternalAdminNetSource2 interface


## -description

The <b>IWMSInternalAdminNetSource2</b> interface provides improved methods for password caching. These methods should be used in preference to their counterparts in <a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource</a> because the older methods are vulnerable to spoofing and are therefore not secure.

To obtain a pointer to an instance of this interface, call the <b>QueryInterface</b> method of the <b>IDispatch</b> method retrieved by <a href="/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-getnetsourceadmininterface">INSNetSourceCreator::GetNetSourceAdminInterface</a>.

## -inheritance

The <b>IWMSInternalAdminNetSource2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMSInternalAdminNetSource2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource3">IWMSInternalAdminNetSource3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
