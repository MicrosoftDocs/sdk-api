---
UID: NN:cluadmex.IWEExtendWizard97
title: IWEExtendWizard97 (cluadmex.h)
author: windows-sdk-content
description: Implement the IWEExtendWizard97 interface to add Wizard97-style wizard pages to a Failover Cluster Administrator wizard.
old-location: mscs\iweextendwizard97.htm
tech.root: MsCS
ms.assetid: 3473dc89-8676-4b13-b3c8-f112c0b9cf8c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWEExtendWizard97, IWEExtendWizard97 interface [Failover Cluster], IWEExtendWizard97 interface [Failover Cluster],described, _wolf_iweextendwizard97, cluadmex/IWEExtendWizard97, mscs.iweextendwizard97
ms.topic: interface
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
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
 - IWEExtendWizard97
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWEExtendWizard97 interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Implement the <b>IWEExtendWizard97</b> interface 
    to add Wizard97-style wizard pages to a 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> wizard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWEExtendWizard97</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWEExtendWizard97</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWEExtendWizard97</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">CreateWizard97Pages</a>
</td>
<td align="left" width="63%">
Allows you to create Wizard 97 wizard pages and add them to a Failover Cluster Administrator wizard.

</td>
</tr>
</table> 


## -remarks



To create non-Wizard97 pages, see <a href="https://msdn.microsoft.com/6407163e-a8ca-4601-88a0-ecf87e29b9ab">IWEExtendWizard</a>.




## -see-also




<a href="https://msdn.microsoft.com/a2306e94-47c6-441f-b06d-70e3f633f78e">Failover Cluster Administrator Extension Interfaces</a>
 

 

