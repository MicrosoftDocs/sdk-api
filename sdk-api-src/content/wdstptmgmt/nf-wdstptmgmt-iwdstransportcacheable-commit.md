---
UID: NF:wdstptmgmt.IWdsTransportCacheable.Commit
title: IWdsTransportCacheable::Commit (wdstptmgmt.h)
description: Commits object data members to the underlying data store if the IWdsTransportCacheable::Dirty property has been set. Otherwise, the method returns with no action.
helpviewer_keywords: ["Commit","Commit method [Windows Deployment Services]","Commit method [Windows Deployment Services]","IWdsTransportCacheable interface","IWdsTransportCacheable interface [Windows Deployment Services]","Commit method","IWdsTransportCacheable.Commit","IWdsTransportCacheable::Commit","wds.iwdstransportcacheable_commit","wdstptmgmt/IWdsTransportCacheable::Commit"]
old-location: wds\iwdstransportcacheable_commit.htm
tech.root: wds
ms.assetid: bd651e56-3945-48ca-a490-e20db88eb2fb
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Deployment Services], Commit method [Windows Deployment Services],IWdsTransportCacheable interface, IWdsTransportCacheable interface [Windows Deployment Services],Commit method, IWdsTransportCacheable.Commit, IWdsTransportCacheable::Commit, wds.iwdstransportcacheable_commit, wdstptmgmt/IWdsTransportCacheable::Commit
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
 - IWdsTransportCacheable::Commit
 - wdstptmgmt/IWdsTransportCacheable::Commit
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
 - IWdsTransportCacheable.Commit
---

# IWdsTransportCacheable::Commit


## -description

Commits object data members to the underlying data store if the <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-get_dirty">IWdsTransportCacheable::Dirty</a> property has been set. Otherwise, the method returns with no action.



## -remarks

Upon successful completion, this method clears the <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcacheable-get_dirty">Dirty</a> property.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcacheable">IWdsTransportCacheable</a>
