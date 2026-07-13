---
UID: NN:wmsinternaladminnetsource.IWMSInternalAdminNetSource3
title: IWMSInternalAdminNetSource3 (wmsinternaladminnetsource.h)
description: The IWMSInternalAdminNetSource3 interface provides improved methods to find proxy servers.To obtain a pointer to an instance of this interface, call the QueryInterface method of the IDispatch method retrieved by INSNetSourceCreator::GetNetSourceAdminInterface.
helpviewer_keywords: ["IWMSInternalAdminNetSource3","IWMSInternalAdminNetSource3 interface [windows Media Format]","IWMSInternalAdminNetSource3 interface [windows Media Format]","described","IWMSInternalAdminNetSource3Interface","wmformat.iwmsinternaladminnetsource3","wmsinternaladminnetsource/IWMSInternalAdminNetSource3"]
old-location: wmformat\iwmsinternaladminnetsource3.htm
tech.root: wmformat
ms.assetid: b4ca08a4-6e2d-4646-b101-67bac67300b1
ms.date: 4/26/2023
ms.keywords: IWMSInternalAdminNetSource3, IWMSInternalAdminNetSource3 interface [windows Media Format], IWMSInternalAdminNetSource3 interface [windows Media Format],described, IWMSInternalAdminNetSource3Interface, wmformat.iwmsinternaladminnetsource3, wmsinternaladminnetsource/IWMSInternalAdminNetSource3
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
 - IWMSInternalAdminNetSource3
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource3
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
 - IWMSInternalAdminNetSource3
 - IWMSInternalAdminNetSource3.GetNetSourceCreator2
 - IWMSInternalAdminNetSource3.IsUsingIE2
 - IWMSInternalAdminNetSource3.RegisterProxyFailure2
---

# IWMSInternalAdminNetSource3 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMSInternalAdminNetSource3</b> interface provides improved methods to find proxy servers.

To obtain a pointer to an instance of this interface, call the <b>QueryInterface</b> method of the <b>IDispatch</b> method retrieved by <a href="/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-getnetsourceadmininterface">INSNetSourceCreator::GetNetSourceAdminInterface</a>.

## -inheritance

The <b>IWMSInternalAdminNetSource3</b> interface inherits from <a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2</a>. <b>IWMSInternalAdminNetSource3</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
