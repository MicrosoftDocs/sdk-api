---
UID: NN:wmsinternaladminnetsource.IWMSInternalAdminNetSource
title: IWMSInternalAdminNetSource (wmsinternaladminnetsource.h)
description: The IWMSInternalAdminNetSource interface manages cached passwords and finds proxy servers.To obtain a pointer to an instance of this interface, call the QueryInterface method of the IDispatch interface retrieved by INSNetSourceCreator::GetNetSourceAdminInterface.
helpviewer_keywords: ["IWMSInternalAdminNetSource","IWMSInternalAdminNetSource interface [windows Media Format]","IWMSInternalAdminNetSource interface [windows Media Format]","described","IWMSInternalAdminNetSourceInterface","wmformat.iwmsinternaladminnetsource","wmsinternaladminnetsource/IWMSInternalAdminNetSource"]
old-location: wmformat\iwmsinternaladminnetsource.htm
tech.root: wmformat
ms.assetid: 0fbdad85-d94a-4598-bb25-f733df33692a
ms.date: 12/05/2018
ms.keywords: IWMSInternalAdminNetSource, IWMSInternalAdminNetSource interface [windows Media Format], IWMSInternalAdminNetSource interface [windows Media Format],described, IWMSInternalAdminNetSourceInterface, wmformat.iwmsinternaladminnetsource, wmsinternaladminnetsource/IWMSInternalAdminNetSource
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
 - IWMSInternalAdminNetSource
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource
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
 - IWMSInternalAdminNetSource
 - IWMSInternalAdminNetSource.GetNetSourceCreator
 - IWMSInternalAdminNetSource.Initialize
 - IWMSInternalAdminNetSource.IsUsingIE
---

# IWMSInternalAdminNetSource interface


## -description

The <b>IWMSInternalAdminNetSource</b> interface manages cached passwords and finds proxy servers.

To obtain a pointer to an instance of this interface, call the <b>QueryInterface</b> method of the <b>IDispatch</b> interface retrieved by <a href="/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-getnetsourceadmininterface">INSNetSourceCreator::GetNetSourceAdminInterface</a>.

## -inheritance

The <b>IWMSInternalAdminNetSource</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMSInternalAdminNetSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

Most of the methods of the <b>IWMSInternalAdminNetSource</b> interface have been updated in <a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2</a> and <a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource3">IWMSInternalAdminNetSource3</a>. If you are developing an application using a version of the Windows Media Format SDK that supports the later interfaces, you should use them.

## -see-also

<a href="/windows/desktop/api/wmnetsourcecreator/nn-wmnetsourcecreator-insnetsourcecreator">INSNetSourceCreator Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2 Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource3">IWMSInternalAdminNetSource3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
