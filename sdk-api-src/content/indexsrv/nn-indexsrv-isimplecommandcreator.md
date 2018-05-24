---
UID: NN:indexsrv.ISimpleCommandCreator
title: ISimpleCommandCreator
author: windows-driver-content
description: Contains methods for interacting with the file catalog.
old-location: search\isimplecommandcreator.htm
old-project: search
ms.assetid: CAC6BE83-863B-4DB0-B4FF-40029C242AE9
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ISimpleCommandCreator, ISimpleCommandCreator interface [search], ISimpleCommandCreator interface [search],described, indexsrv/ISimpleCommandCreator, search.isimplecommandcreator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WORDREP_BREAK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	indexsrv.h
api_name:
-	ISimpleCommandCreator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISimpleCommandCreator interface


## -description


Contains methods for interacting with the file catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimpleCommandCreator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimpleCommandCreator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/70880905-E4DF-4064-A877-18AF5CE839FB">CreateICommand</a>
</td>
<td align="left" width="63%">
Creates an ICommand.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6BD65290-209A-4FCA-BD2B-E4BB800C8BEF">GetDefaultCatalog</a>
</td>
<td align="left" width="63%">
Determines the default catalog for the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F4B1558D-F244-40ED-92C2-F5CC0B63AD50">VerifyCatalog</a>
</td>
<td align="left" width="63%">
Validates the catalog location.

</td>
</tr>
</table> 

