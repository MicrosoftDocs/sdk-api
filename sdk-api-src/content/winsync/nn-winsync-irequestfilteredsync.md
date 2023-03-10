---
UID: NN:winsync.IRequestFilteredSync
title: IRequestFilteredSync (winsync.h)
description: When implemented by a derived class, represents a destination provider that can specify a filter to be used by the source provider during change enumeration.
helpviewer_keywords: ["IRequestFilteredSync","IRequestFilteredSync interface [Windows Sync]","IRequestFilteredSync interface [Windows Sync]","described","winsync.irequestfilteredsync","winsync/IRequestFilteredSync"]
old-location: winsync\irequestfilteredsync.htm
tech.root: winsync
ms.assetid: e4b76bb3-d572-4441-94db-7088e881ede2
ms.date: 12/05/2018
ms.keywords: IRequestFilteredSync, IRequestFilteredSync interface [Windows Sync], IRequestFilteredSync interface [Windows Sync],described, winsync.irequestfilteredsync, winsync/IRequestFilteredSync
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
 - IRequestFilteredSync
 - winsync/IRequestFilteredSync
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
 - IRequestFilteredSync
---

# IRequestFilteredSync interface


## -description

When implemented by a derived class, represents a destination provider that can specify a filter to be used by the source provider during change enumeration.

## -inheritance

The <b>IRequestFilteredSync</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRequestFilteredSync</b> also has these types of members:

## -remarks

Typically, <b>IRequestFilteredSync</b> is implemented by a destination provider.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
