---
UID: NN:wmnetsourcecreator.INSNetSourceCreator
title: INSNetSourceCreator (wmnetsourcecreator.h)
description: The INSNetSourceCreator interface creates an administrative network source plug-in.
old-location: wmformat\insnetsourcecreator.htm
tech.root: wmformat
ms.assetid: 39e692a6-fb68-447f-bd28-8d216776157a
ms.date: 12/05/2018
ms.keywords: INSNetSourceCreator, INSNetSourceCreator interface [windows Media Format], INSNetSourceCreator interface [windows Media Format],described, INSNetSourceCreatorInterface, wmformat.insnetsourcecreator, wmnetsourcecreator/INSNetSourceCreator
f1_keywords:
- wmnetsourcecreator/INSNetSourceCreator
dev_langs:
- c++
req.header: wmnetsourcecreator.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmnetsourcecreator.h
api_name:
- INSNetSourceCreator
- INSNetSourceCreator.CreateNetSource
- INSNetSourceCreator.GetNetSourceProperties
- INSNetSourceCreator.GetNetSourceSharedNamespace
- INSNetSourceCreator.GetNumProtocolsSupported
- INSNetSourceCreator.GetProtocolName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INSNetSourceCreator interface


## -description



The <b>INSNetSourceCreator</b> interface creates an administrative network source <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">plug-in</a>. You can use an administrative network source plug-in to cache passwords and to locate the appropriate proxy server to use for Internet operations.

To get a pointer to the <b>INSNetSourceCreator</b> interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with <b>CLSID_ClientNetManager</b> as the <i>REFCLSID</i> parameter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INSNetSourceCreator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INSNetSourceCreator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INSNetSourceCreator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CreateNetSource</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-getnetsourceadmininterface">GetNetSourceAdminInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an administrative network source object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetNetSourceProperties</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetNetSourceSharedNamespace</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetNumProtocolsSupported</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetProtocolName</b></td>
<td align="left" width="63%">
Reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the network source creator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the network source creator.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

