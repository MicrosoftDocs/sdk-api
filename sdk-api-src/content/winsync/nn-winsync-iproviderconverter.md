---
UID: NN:winsync.IProviderConverter
title: IProviderConverter (winsync.h)
description: When implemented by a derived class, represents an object that can convert an ISyncProvider object to an IKnowledgeSyncProvider object.
helpviewer_keywords: ["IProviderConverter","IProviderConverter interface [Windows Sync]","IProviderConverter interface [Windows Sync]","described","winsync.iproviderconverter","winsync/IProviderConverter"]
old-location: winsync\iproviderconverter.htm
tech.root: winsync
ms.assetid: 67dc6290-00e8-457a-97be-efe8e731619d
ms.date: 12/05/2018
ms.keywords: IProviderConverter, IProviderConverter interface [Windows Sync], IProviderConverter interface [Windows Sync],described, winsync.iproviderconverter, winsync/IProviderConverter
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
 - IProviderConverter
 - winsync/IProviderConverter
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
 - IProviderConverter
---

# IProviderConverter interface


## -description

When implemented by a derived class, represents an object that can convert an <b>ISyncProvider</b> object to an <b>IKnowledgeSyncProvider</b> object.

## -inheritance

The <b>IProviderConverter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProviderConverter</b> also has these types of members:

## -remarks

<b>IProviderConverter</b> is typically implemented by the developer of the custom provider that it converts.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
