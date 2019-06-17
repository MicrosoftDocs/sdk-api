---
UID: NN:mergemod.IMsmConfigureModule
title: IMsmConfigureModule (mergemod.h)
author: windows-sdk-content
description: The IMsmConfigureModule interface is a callback interface; it enables the client to provide merge configuration information during the merge process.
old-location: setup\imsmconfiguremodule_interface.htm
tech.root: Msi
ms.assetid: 90e09449-6211-4eae-8fd1-446e0187ed6c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMsmConfigureModule, IMsmConfigureModule interface, IMsmConfigureModule interface,described, mergemod/IMsmConfigureModule, setup.imsmconfiguremodule_interface
ms.topic: interface
f1_keywords: ["mergemod/IMsmConfigureModule"]
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmConfigureModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmConfigureModule interface


## -description


The <b>IMsmConfigureModule</b> interface is a callback interface; it enables the client to provide merge configuration information during the
merge process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmConfigureModule</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmConfigureModule</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmConfigureModule</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata">ProvideIntegerData</a>
</td>
<td align="left" width="63%">
Retrieves integer data from the client tool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfiguremodule-providetextdata">ProvideTextData</a>
</td>
<td align="left" width="63%">
Retrieves text data from the client tool.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>
 

 

