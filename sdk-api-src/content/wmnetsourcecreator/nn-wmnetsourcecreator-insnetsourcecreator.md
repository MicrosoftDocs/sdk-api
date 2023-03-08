---
UID: NN:wmnetsourcecreator.INSNetSourceCreator
title: INSNetSourceCreator (wmnetsourcecreator.h)
description: The INSNetSourceCreator interface creates an administrative network source plug-in.
helpviewer_keywords: ["INSNetSourceCreator","INSNetSourceCreator interface [windows Media Format]","INSNetSourceCreator interface [windows Media Format]","described","INSNetSourceCreatorInterface","wmformat.insnetsourcecreator","wmnetsourcecreator/INSNetSourceCreator"]
old-location: wmformat\insnetsourcecreator.htm
tech.root: wmformat
ms.assetid: 39e692a6-fb68-447f-bd28-8d216776157a
ms.date: 12/05/2018
ms.keywords: INSNetSourceCreator, INSNetSourceCreator interface [windows Media Format], INSNetSourceCreator interface [windows Media Format],described, INSNetSourceCreatorInterface, wmformat.insnetsourcecreator, wmnetsourcecreator/INSNetSourceCreator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INSNetSourceCreator
 - wmnetsourcecreator/INSNetSourceCreator
dev_langs:
 - c++
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
---

# INSNetSourceCreator interface


## -description

The <b>INSNetSourceCreator</b> interface creates an administrative network source <a href="/windows/desktop/wmformat/wmformat-glossary">plug-in</a>. You can use an administrative network source plug-in to cache passwords and to locate the appropriate proxy server to use for Internet operations.

To get a pointer to the <b>INSNetSourceCreator</b> interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with <b>CLSID_ClientNetManager</b> as the <i>REFCLSID</i> parameter.

## -inheritance

The <b>INSNetSourceCreator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INSNetSourceCreator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
