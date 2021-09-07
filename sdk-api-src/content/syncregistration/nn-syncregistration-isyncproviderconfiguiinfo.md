---
UID: NN:syncregistration.ISyncProviderConfigUIInfo
title: ISyncProviderConfigUIInfo (syncregistration.h)
description: Represents the information and properties needed to create an instance of a synchronization provider configuration UI.
helpviewer_keywords: ["ISyncProviderConfigUIInfo","ISyncProviderConfigUIInfo interface [Windows Sync]","ISyncProviderConfigUIInfo interface [Windows Sync]","described","syncregistration/ISyncProviderConfigUIInfo","winsync.isyncproviderconfiguiinfo"]
old-location: winsync\isyncproviderconfiguiinfo.htm
tech.root: winsync
ms.assetid: b7c49533-d289-44b0-9a9e-cfa47af3a087
ms.date: 12/05/2018
ms.keywords: ISyncProviderConfigUIInfo, ISyncProviderConfigUIInfo interface [Windows Sync], ISyncProviderConfigUIInfo interface [Windows Sync],described, syncregistration/ISyncProviderConfigUIInfo, winsync.isyncproviderconfiguiinfo
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
 - ISyncProviderConfigUIInfo
 - syncregistration/ISyncProviderConfigUIInfo
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
 - ISyncProviderConfigUIInfo
---

# ISyncProviderConfigUIInfo interface


## -description

Represents the information and properties needed to create an instance of a synchronization provider configuration UI.

## -inheritance

The <b>ISyncProviderConfigUIInfo</b> interface inherits from <b>IPropertyStore</b>. <b>ISyncProviderConfigUIInfo</b> also has these types of members:

## -remarks

You can get and set the properties of a  synchronization provider configuration UI by calling the <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderconfiguiinfo-getsyncproviderconfigui">GetSyncProviderConfigUI</a> method and manipulating the configuration UI's <b>IPropertyStore</b>.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
