---
UID: NN:cluadmex.IWCPropertySheetCallback
title: IWCPropertySheetCallback
author: windows-sdk-content
description: The IWCPropertySheetCallback interface is called by a Failover Cluster Administrator extension to add property pages to a Failover Cluster Administrator property sheet.
old-location: mscs\iwcpropertysheetcallback.htm
tech.root: mscs
ms.assetid: f90f9eb3-5568-4db1-8ff8-fda2d3bea952
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IWCPropertySheetCallback, IWCPropertySheetCallback interface [Failover Cluster], IWCPropertySheetCallback interface [Failover Cluster],described, _wolf_iwcpropertysheetcallback, cluadmex/IWCPropertySheetCallback, mscs.iwcpropertysheetcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
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
 - cluadmex.h
api_name:
 - IWCPropertySheetCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWCPropertySheetCallback interface


## -description


The <b>IWCPropertySheetCallback</b> interface is 
    called by a <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extension 
    to add property pages to a Failover Cluster Administrator property sheet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWCPropertySheetCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWCPropertySheetCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWCPropertySheetCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccd87d3a-c9da-4d61-9e9b-f25a52724166">AddPropertySheetPage</a>
</td>
<td align="left" width="63%">
Adds a property page to a Failover Cluster Administrator property sheet.

</td>
</tr>
</table> 


## -remarks



Use the <i>piCallback</i> pointer that you receive when Failover Cluster Administrator calls 
     your 
     <a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a> 
     method to call the <b>IWCPropertySheetCallback</b> 
     interface.




## -see-also




<a href="https://msdn.microsoft.com/4a2b0c21-1b3f-4037-a143-02956e6996ce">Failover Cluster Administrator Callback Interfaces</a>



<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>
 

 

