---
UID: NN:indexsrv.ISimpleCommandCreator
title: ISimpleCommandCreator (indexsrv.h)
description: Contains methods for interacting with the file catalog.
old-location: search\isimplecommandcreator.htm
tech.root: search
ms.assetid: CAC6BE83-863B-4DB0-B4FF-40029C242AE9
ms.date: 12/05/2018
ms.keywords: ISimpleCommandCreator, ISimpleCommandCreator interface [search], ISimpleCommandCreator interface [search],described, indexsrv/ISimpleCommandCreator, search.isimplecommandcreator
ms.topic: interface
f1_keywords:
- indexsrv/ISimpleCommandCreator
dev_langs:
- c++
req.header: indexsrv.h
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
- indexsrv.h
api_name:
- ISimpleCommandCreator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimpleCommandCreator interface


## -description


Contains methods for interacting with the file catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimpleCommandCreator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimpleCommandCreator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimpleCommandCreator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-isimplecommandcreator-createicommand">CreateICommand</a>
</td>
<td align="left" width="63%">
Creates an ICommand.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-isimplecommandcreator-getdefaultcatalog">GetDefaultCatalog</a>
</td>
<td align="left" width="63%">
Determines the default catalog for the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-isimplecommandcreator-verifycatalog">VerifyCatalog</a>
</td>
<td align="left" width="63%">
Validates the catalog location.

</td>
</tr>
</table> 

