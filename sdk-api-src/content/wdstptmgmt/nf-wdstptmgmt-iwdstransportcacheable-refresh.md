---
UID: NF:wdstptmgmt.IWdsTransportCacheable.Refresh
title: IWdsTransportCacheable::Refresh (wdstptmgmt.h)
description: Refreshes the object data members by rereading their values from the underlying data store. This is allowed only if the object's IWdsTransportCacheable::Dirty property has been set.
helpviewer_keywords: ["IWdsTransportCacheable interface [Windows Deployment Services]","Refresh method","IWdsTransportCacheable.Refresh","IWdsTransportCacheable::Refresh","Refresh","Refresh method [Windows Deployment Services]","Refresh method [Windows Deployment Services]","IWdsTransportCacheable interface","wds.iwdstransportcacheable_refresh","wdstptmgmt/IWdsTransportCacheable::Refresh"]
old-location: wds\iwdstransportcacheable_refresh.htm
tech.root: wds
ms.assetid: 2fd838b5-5623-4133-9ad8-ec051b2b698d
ms.date: 12/05/2018
ms.keywords: IWdsTransportCacheable interface [Windows Deployment Services],Refresh method, IWdsTransportCacheable.Refresh, IWdsTransportCacheable::Refresh, Refresh, Refresh method [Windows Deployment Services], Refresh method [Windows Deployment Services],IWdsTransportCacheable interface, wds.iwdstransportcacheable_refresh, wdstptmgmt/IWdsTransportCacheable::Refresh
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWdsTransportCacheable::Refresh
 - wdstptmgmt/IWdsTransportCacheable::Refresh
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportCacheable.Refresh
---

# IWdsTransportCacheable::Refresh


## -description

Refreshes the object data members by rereading their values from the underlying data store. This is allowed only if the object's <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-get_dirty">IWdsTransportCacheable::Dirty</a> property has been set.



## -remarks

When called on an object whose <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-get_dirty">Dirty</a> property has been set, this method fails in order to avoid inadvertently losing changes made to the object. If the caller wants to ignore current changes and reread the stored data, the caller should call the <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-discard">IWdsTransportCacheable::Discard</a> method instead.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcacheable">IWdsTransportCacheable</a>
