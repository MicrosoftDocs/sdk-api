---
UID: NN:ndhelper.INetDiagHelperInfo
title: INetDiagHelperInfo
author: windows-sdk-content
description: The INetDiagHelperInfo interface provides a method that is called by the Network Diagnostics Framework (NDF) when it needs to validate that it has the necessary information for a helper class and that it has chosen the correct helper class.
old-location: ndf\inetdiaghelperinfo.htm
tech.root: NDF
ms.assetid: 815e2338-0055-4078-a9a5-197db449c33d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetDiagHelperInfo, INetDiagHelperInfo interface [NDF], INetDiagHelperInfo interface [NDF],described, ndf.inetdiaghelperinfo, ndhelper/INetDiagHelperInfo
ms.topic: interface
req.header: ndhelper.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ndhelper.h
api_name:
 - INetDiagHelperInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetDiagHelperInfo interface


## -description


The <b>INetDiagHelperInfo</b> interface provides a method that is called by the Network Diagnostics Framework (NDF) when it needs to validate that it has the necessary information for a helper class and that it has chosen the correct helper class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetDiagHelperInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetDiagHelperInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetDiagHelperInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c1a12f3-357f-4d96-b0ef-99d788b6e020">INetDiagHelperInfo::GetAttributeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the list of key parameters required by the Helper Class Extension.

</td>
</tr>
</table> 

