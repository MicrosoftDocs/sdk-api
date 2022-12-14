---
UID: NN:cluadmex.IWCPropertySheetCallback
title: IWCPropertySheetCallback (cluadmex.h)
description: The IWCPropertySheetCallback interface is called by a Failover Cluster Administrator extension to add property pages to a Failover Cluster Administrator property sheet.
helpviewer_keywords: ["IWCPropertySheetCallback","IWCPropertySheetCallback interface [Failover Cluster]","IWCPropertySheetCallback interface [Failover Cluster]","described","_wolf_iwcpropertysheetcallback","cluadmex/IWCPropertySheetCallback","mscs.iwcpropertysheetcallback"]
old-location: mscs\iwcpropertysheetcallback.htm
tech.root: MsCS
ms.assetid: f90f9eb3-5568-4db1-8ff8-fda2d3bea952
ms.date: 12/05/2018
ms.keywords: IWCPropertySheetCallback, IWCPropertySheetCallback interface [Failover Cluster], IWCPropertySheetCallback interface [Failover Cluster],described, _wolf_iwcpropertysheetcallback, cluadmex/IWCPropertySheetCallback, mscs.iwcpropertysheetcallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWCPropertySheetCallback
 - cluadmex/IWCPropertySheetCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IWCPropertySheetCallback
---

# IWCPropertySheetCallback interface


## -description

The <b>IWCPropertySheetCallback</b> interface is 
    called by a <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extension 
    to add property pages to a Failover Cluster Administrator property sheet.

## -inheritance

The <b>IWCPropertySheetCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWCPropertySheetCallback</b> also has these types of members:

## -remarks

Use the <i>piCallback</i> pointer that you receive when Failover Cluster Administrator calls 
     your 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a> 
     method to call the <b>IWCPropertySheetCallback</b> 
     interface.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-callback-interfaces">Failover Cluster Administrator Callback Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>
