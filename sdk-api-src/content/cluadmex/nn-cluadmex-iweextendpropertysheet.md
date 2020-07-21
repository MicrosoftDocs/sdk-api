---
UID: NN:cluadmex.IWEExtendPropertySheet
title: IWEExtendPropertySheet (cluadmex.h)
description: Implement the IWEExtendPropertySheet interface to create property sheet pages for a cluster object and add them to a Failover Cluster Administrator property sheet.
helpviewer_keywords: ["IWEExtendPropertySheet","IWEExtendPropertySheet interface [Failover Cluster]","IWEExtendPropertySheet interface [Failover Cluster]","described","_wolf_iweextendpropertysheet","cluadmex/IWEExtendPropertySheet","mscs.iweextendpropertysheet"]
old-location: mscs\iweextendpropertysheet.htm
tech.root: MsCS
ms.assetid: 1f2b7760-24d3-44a7-96a0-87e153b4bf92
ms.date: 12/05/2018
ms.keywords: IWEExtendPropertySheet, IWEExtendPropertySheet interface [Failover Cluster], IWEExtendPropertySheet interface [Failover Cluster],described, _wolf_iweextendpropertysheet, cluadmex/IWEExtendPropertySheet, mscs.iweextendpropertysheet
f1_keywords:
- cluadmex/IWEExtendPropertySheet
dev_langs:
- c++
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
- IWEExtendPropertySheet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWEExtendPropertySheet interface


## -description


Implement the <b>IWEExtendPropertySheet</b> 
    interface to create property sheet pages for a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster object</a> and add them to a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> property 
    sheet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWEExtendPropertySheet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWEExtendPropertySheet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWEExtendPropertySheet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">CreatePropertySheetPages</a>
</td>
<td align="left" width="63%">
Allows you to create property pages for a cluster object and add them to a Failover Cluster Administrator 
      property sheet.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator-extension-interfaces">Failover Cluster Administrator Extension Interfaces</a>
 

 

