---
UID: NN:mergemod.IMsmGetFiles
title: IMsmGetFiles (mergemod.h)
description: The IMsmGetFiles interface enables the client to retrieve the files needed in a particular language of the module.helpviewer_keywords: ["IMsmGetFiles","IMsmGetFiles interface","IMsmGetFiles interface","described","mergemod/IMsmGetFiles","setup.imsmgetfiles_interface"]
old-location: setup\imsmgetfiles_interface.htm
tech.root: Msi
ms.assetid: d6912c92-b3e0-4b3d-a618-17e252cd14ae
ms.date: 12/05/2018
ms.keywords: IMsmGetFiles, IMsmGetFiles interface, IMsmGetFiles interface,described, mergemod/IMsmGetFiles, setup.imsmgetfiles_interface
f1_keywords:
- mergemod/IMsmGetFiles
dev_langs:
- c++
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
- IMsmGetFiles
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmGetFiles interface


## -description


The <b>IMsmGetFiles</b> interface enables the client to retrieve the files needed in a particular language of the
 module.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmGetFiles</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmGetFiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmGetFiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles">get_ModuleFiles</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/getfiles-modulefiles">ModuleFiles</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/getfiles-object">GetFiles</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>
 

 

