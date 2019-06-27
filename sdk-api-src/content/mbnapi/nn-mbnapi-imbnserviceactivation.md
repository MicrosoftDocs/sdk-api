---
UID: NN:mbnapi.IMbnServiceActivation
title: IMbnServiceActivation (mbnapi.h)
author: windows-sdk-content
description: Pass-through mechanism for cellular service activation.
old-location: mbn\imbnserviceactivation.htm
tech.root: mbn
ms.assetid: cf23be24-f7a8-41b9-81f1-c267a265f85b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnServiceActivation, IMbnServiceActivation interface [Microsoft Broadband Networks], IMbnServiceActivation interface [Microsoft Broadband Networks],described, mbn.imbnserviceactivation, mbnapi/IMbnServiceActivation
ms.topic: interface
f1_keywords: 
 - "mbnapi/IMbnServiceActivation"
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnServiceActivation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnServiceActivation interface


## -description


Pass-through mechanism for cellular service activation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnServiceActivation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnServiceActivation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnServiceActivation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnserviceactivation-activate">Activate</a>
</td>
<td align="left" width="63%">
Sends the service activation request to the network.

</td>
</tr>
</table> 


## -remarks



An <b>IMbnServiceActivation</b> interface can be obtained by calling <b>QueryInterface</b>  from <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.



