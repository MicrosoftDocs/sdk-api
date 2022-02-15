---
UID: NN:syncregistration.IEnumSyncProviderInfos
title: IEnumSyncProviderInfos (syncregistration.h)
description: Enumerates ISyncProviderInfo objects that contain the information used to create an instance of a synchronization provider.
helpviewer_keywords: ["IEnumSyncProviderInfos","IEnumSyncProviderInfos interface [Windows Sync]","IEnumSyncProviderInfos interface [Windows Sync]","described","syncregistration/IEnumSyncProviderInfos","winsync.ienumsyncproviderinfos"]
old-location: winsync\ienumsyncproviderinfos.htm
tech.root: winsync
ms.assetid: 58b0dcc2-861a-4138-872a-cbbe2bb2cc4d
ms.date: 12/05/2018
ms.keywords: IEnumSyncProviderInfos, IEnumSyncProviderInfos interface [Windows Sync], IEnumSyncProviderInfos interface [Windows Sync],described, syncregistration/IEnumSyncProviderInfos, winsync.ienumsyncproviderinfos
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
 - IEnumSyncProviderInfos
 - syncregistration/IEnumSyncProviderInfos
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
 - IEnumSyncProviderInfos
---

# IEnumSyncProviderInfos interface


## -description

Enumerates <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderInfo</a> objects that contain the information used to create an instance of a synchronization provider.

## -inheritance

The <b>IEnumSyncProviderInfos</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncProviderInfos</b> also has these types of members:

## -remarks

This interface is obtained from the  <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-enumeratesyncproviders">ISyncProviderRegistration::EnumerateSyncProviders</a> method. The method will return an  <b>IEnumSyncProviderInfos</b> enumerator for all registered <b>ISyncProviderInfo</b> objects or for just the registered <b>ISyncProviderInfo</b> objects that match the particular filter criteria.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
