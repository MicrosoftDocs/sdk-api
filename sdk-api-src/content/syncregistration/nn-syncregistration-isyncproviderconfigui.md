---
UID: NN:syncregistration.ISyncProviderConfigUI
title: ISyncProviderConfigUI (syncregistration.h)
description: Represents configuration UI information used to build and register a synchronization provider.
helpviewer_keywords: ["ISyncProviderConfigUI","ISyncProviderConfigUI interface [Windows Sync]","ISyncProviderConfigUI interface [Windows Sync]","described","syncregistration/ISyncProviderConfigUI","winsync.isyncproviderconfigui"]
old-location: winsync\isyncproviderconfigui.htm
tech.root: winsync
ms.assetid: 27757aa1-a42d-4f66-99a8-bf66385fbec1
ms.date: 12/05/2018
ms.keywords: ISyncProviderConfigUI, ISyncProviderConfigUI interface [Windows Sync], ISyncProviderConfigUI interface [Windows Sync],described, syncregistration/ISyncProviderConfigUI, winsync.isyncproviderconfigui
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
 - ISyncProviderConfigUI
 - syncregistration/ISyncProviderConfigUI
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
 - ISyncProviderConfigUI
---

# ISyncProviderConfigUI interface


## -description

Represents configuration UI information used to build and register a synchronization provider.

## -inheritance

The <b>ISyncProviderConfigUI</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncProviderConfigUI</b> also has these types of members:

## -remarks

The writer of a synchronization provider should implement an <b>ISyncProviderConfigUI</b> (a builder) for a synchronization provider if it requires additional information and properties to be set before it can be created. For example, a synchronization provider may require a user to enter credentials before their data can be synchronized.

If the registered synchronization provider is a <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a> provider, then the <b>Init</b> method will be called by the Sync Framework synchronization session. For more information about the different types of synchronization providers you can write for Windows, see <a href="/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
