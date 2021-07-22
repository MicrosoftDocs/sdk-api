---
UID: NN:winsync.ISupportFilteredSync
title: ISupportFilteredSync (winsync.h)
description: When implemented by a derived class, represents a source provider that supports filtered change enumeration, and that can negotiate the type of filter that is used.
helpviewer_keywords: ["ISupportFilteredSync","ISupportFilteredSync interface [Windows Sync]","ISupportFilteredSync interface [Windows Sync]","described","winsync.isupportfilteredsync","winsync/ISupportFilteredSync"]
old-location: winsync\isupportfilteredsync.htm
tech.root: winsync
ms.assetid: cf07e322-7c75-49a4-a514-b4c782ceb2d7
ms.date: 12/05/2018
ms.keywords: ISupportFilteredSync, ISupportFilteredSync interface [Windows Sync], ISupportFilteredSync interface [Windows Sync],described, winsync.isupportfilteredsync, winsync/ISupportFilteredSync
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISupportFilteredSync
 - winsync/ISupportFilteredSync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISupportFilteredSync
---

# ISupportFilteredSync interface


## -description

When implemented by a derived class, represents a source provider that supports filtered change enumeration, and that can negotiate the type of filter that is used.

## -inheritance

The <b>ISupportFilteredSync</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISupportFilteredSync</b> also has these types of members:

## -remarks

<b>ISupportFilteredSync</b> is typically implemented by a source provider.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ifilterrequestcallback">IFilterRequestCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irequestfilteredsync">IRequestFilteredSync Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
