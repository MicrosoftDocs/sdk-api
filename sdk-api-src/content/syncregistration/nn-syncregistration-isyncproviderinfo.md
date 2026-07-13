---
UID: NN:syncregistration.ISyncProviderInfo
title: ISyncProviderInfo (syncregistration.h)
description: Represents the information and properties needed to create an instance of a synchronization provider.
helpviewer_keywords: ["ISyncProviderInfo","ISyncProviderInfo interface [Windows Sync]","ISyncProviderInfo interface [Windows Sync]","described","syncregistration/ISyncProviderInfo","winsync.isyncproviderinfo"]
old-location: winsync\isyncproviderinfo.htm
tech.root: winsync
ms.assetid: fe50e34c-6499-4c1e-b891-7b4f797510f2
ms.date: 12/05/2018
ms.keywords: ISyncProviderInfo, ISyncProviderInfo interface [Windows Sync], ISyncProviderInfo interface [Windows Sync],described, syncregistration/ISyncProviderInfo, winsync.isyncproviderinfo
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
 - ISyncProviderInfo
 - syncregistration/ISyncProviderInfo
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
 - ISyncProviderInfo
---

# ISyncProviderInfo interface


## -description

Represents the information and properties needed to create an instance of a synchronization provider.

## -inheritance

The <b>ISyncProviderInfo</b> interface inherits from <b>IPropertyStore</b>. <b>ISyncProviderInfo</b> also has these types of members:

## -remarks

This interface is created from the <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration</a> interface and then subsequently registered.  It is the mechanism by which applications can set the context and UX properties for a synchronization provider by first retrieving the property store and then modifying it.

The properties that are set in  <b>ISyncProviderInfo</b> are written to the registration store by calling the <b>ISyncProviderInfo::Commit</b> method inherited from the <b>IPropertyStore</b> interface. For an example of this, see <a href="/previous-versions/windows/desktop/winsync/overview-of-registering-a-synchronization-provider">Overview of Registering a Synchronization Provider</a>.

You can get and set the properties of a  synchronization provider by calling the <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderinfo-getsyncprovider">GetSyncProvider</a> method and manipulating the provider's <b>IPropertyStore</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>



<a href="/previous-versions/windows/desktop/winsync/overview-of-registering-a-synchronization-provider">Overview of Registering a Synchronization Provider</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
