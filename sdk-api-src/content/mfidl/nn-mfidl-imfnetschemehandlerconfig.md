---
UID: NN:mfidl.IMFNetSchemeHandlerConfig
title: IMFNetSchemeHandlerConfig (mfidl.h)
description: Configures a network scheme plug-in.
old-location: mf\imfnetschemehandlerconfig.htm
tech.root: medfound
ms.assetid: 91bdcdbd-d621-42e3-8e0f-f8eeab489d35
ms.date: 12/05/2018
ms.keywords: 91bdcdbd-d621-42e3-8e0f-f8eeab489d35, IMFNetSchemeHandlerConfig, IMFNetSchemeHandlerConfig interface [Media Foundation], IMFNetSchemeHandlerConfig interface [Media Foundation],described, mf.imfnetschemehandlerconfig, mfidl/IMFNetSchemeHandlerConfig
f1_keywords:
- mfidl/IMFNetSchemeHandlerConfig
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
- IMFNetSchemeHandlerConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetSchemeHandlerConfig interface


## -description


Configures a network scheme plug-in.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetSchemeHandlerConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetSchemeHandlerConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetSchemeHandlerConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols">GetNumberOfSupportedProtocols</a>
</td>
<td align="left" width="63%">
Retrieves the number of protocols supported by the network scheme plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype">GetSupportedProtocolType</a>
</td>
<td align="left" width="63%">
Retrieves the protocol type for a given protocol index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-resetprotocolrolloversettings">ResetProtocolRolloverSettings</a>
</td>
<td align="left" width="63%">
Not implemented in this release.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/supported-protocols">Supported Protocols</a>
 

 

