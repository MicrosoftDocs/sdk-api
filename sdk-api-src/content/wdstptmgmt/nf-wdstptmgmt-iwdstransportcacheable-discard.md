---
UID: NF:wdstptmgmt.IWdsTransportCacheable.Discard
title: IWdsTransportCacheable::Discard (wdstptmgmt.h)
description: Discards all changes made to the object data members by clearing the IWdsTransportCacheable::Dirty property and then calling the object's IWdsTransportCacheable::Refresh method to reread the current object data.
helpviewer_keywords: ["Discard","Discard method [Windows Deployment Services]","Discard method [Windows Deployment Services]","IWdsTransportCacheable interface","IWdsTransportCacheable interface [Windows Deployment Services]","Discard method","IWdsTransportCacheable.Discard","IWdsTransportCacheable::Discard","wds.iwdstransportcacheable_discard","wdstptmgmt/IWdsTransportCacheable::Discard"]
old-location: wds\iwdstransportcacheable_discard.htm
tech.root: wds
ms.assetid: 5c8495b9-6c76-4bb0-8237-5f9008cefc91
ms.date: 12/05/2018
ms.keywords: Discard, Discard method [Windows Deployment Services], Discard method [Windows Deployment Services],IWdsTransportCacheable interface, IWdsTransportCacheable interface [Windows Deployment Services],Discard method, IWdsTransportCacheable.Discard, IWdsTransportCacheable::Discard, wds.iwdstransportcacheable_discard, wdstptmgmt/IWdsTransportCacheable::Discard
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
 - IWdsTransportCacheable::Discard
 - wdstptmgmt/IWdsTransportCacheable::Discard
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
 - IWdsTransportCacheable.Discard
---

# IWdsTransportCacheable::Discard


## -description

Discards all changes made to the object data members by clearing the <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-get_dirty">IWdsTransportCacheable::Dirty</a> property and then calling the object's <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-refresh">IWdsTransportCacheable::Refresh</a> method to reread the current object data.



## -remarks

This method can be called on any object. 

Unlike <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-refresh">Refresh</a>, which always refreshes object data (as long as the object's <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-get_dirty">Dirty</a> property has been set), this method checks first that the object's <b>Dirty</b> property has been set. If it has, the method resets the <b>Dirty</b> property and then rereads the current values of all data members. If <b>Dirty</b> has not been set, this method takes no action and returns immediately.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcacheable">IWdsTransportCacheable</a>
