---
UID: NN:syncregistration.ISyncProviderRegistration
title: ISyncProviderRegistration (syncregistration.h)
description: Represents synchronization provider registration.
helpviewer_keywords: ["ISyncProviderRegistration","ISyncProviderRegistration interface [Windows Sync]","ISyncProviderRegistration interface [Windows Sync]","described","syncregistration/ISyncProviderRegistration","winsync.isyncproviderregistration"]
old-location: winsync\isyncproviderregistration.htm
tech.root: winsync
ms.assetid: e7cf0c05-9d07-4630-ae34-9a9dd81492b2
ms.date: 12/05/2018
ms.keywords: ISyncProviderRegistration, ISyncProviderRegistration interface [Windows Sync], ISyncProviderRegistration interface [Windows Sync],described, syncregistration/ISyncProviderRegistration, winsync.isyncproviderregistration
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
 - ISyncProviderRegistration
 - syncregistration/ISyncProviderRegistration
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
 - ISyncProviderRegistration
---

# ISyncProviderRegistration interface


## -description

Represents synchronization provider registration. This is the core registration interface that contains methods for creating, modifying, and enumerating registered synchronization providers and configuration UIs. This interface can be retrieved by calling <b>CoCreate</b>.

## -inheritance

The <b>ISyncProviderRegistration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncProviderRegistration</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
