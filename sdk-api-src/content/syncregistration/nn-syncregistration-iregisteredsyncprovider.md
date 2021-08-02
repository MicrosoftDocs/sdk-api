---
UID: NN:syncregistration.IRegisteredSyncProvider
title: IRegisteredSyncProvider (syncregistration.h)
description: Represents a registered synchronization provider. This interface is implemented by the writer of a synchronization provider.
helpviewer_keywords: ["IRegisteredSyncProvider","IRegisteredSyncProvider interface [Windows Sync]","IRegisteredSyncProvider interface [Windows Sync]","described","syncregistration/IRegisteredSyncProvider","winsync.iregisteredsyncprovider"]
old-location: winsync\iregisteredsyncprovider.htm
tech.root: winsync
ms.assetid: 53970f17-2857-4624-8594-069cceb93b1e
ms.date: 12/05/2018
ms.keywords: IRegisteredSyncProvider, IRegisteredSyncProvider interface [Windows Sync], IRegisteredSyncProvider interface [Windows Sync],described, syncregistration/IRegisteredSyncProvider, winsync.iregisteredsyncprovider
req.header: syncregistration.h
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
 - IRegisteredSyncProvider
 - syncregistration/IRegisteredSyncProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - IRegisteredSyncProvider
---

# IRegisteredSyncProvider interface


## -description

Represents a registered synchronization provider. This interface is implemented by the writer of a synchronization provider.

## -inheritance

The <b>IRegisteredSyncProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRegisteredSyncProvider</b> also has these types of members:

## -remarks

If the registered synchronization provider is a <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a> provider, then the <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-iregisteredsyncprovider-init">Init</a> method will be called by the Sync Framework synchronization session. For more information about the different types of synchronization providers you can write for Windows, see <a href="/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
