---
UID: NF:sbtsv.ITsSbResourcePluginStore.DeleteTarget
title: ITsSbResourcePluginStore::DeleteTarget (sbtsv.h)
description: Deletes a target.
helpviewer_keywords: ["DeleteTarget","DeleteTarget method [Remote Desktop Services]","DeleteTarget method [Remote Desktop Services]","ITsSbResourcePluginStore interface","DeleteTarget method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","DeleteTarget method","ITsSbResourcePluginStore.DeleteTarget","ITsSbResourcePluginStore::DeleteTarget","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","DeleteTarget method","ITsSbResourcePluginStoreEx::DeleteTarget","sbtsv/ITsSbResourcePluginStore::DeleteTarget","sbtsv/ITsSbResourcePluginStoreEx::DeleteTarget","termserv.itssbresourcepluginstore_deletetarget"]
old-location: termserv\itssbresourcepluginstore_deletetarget.htm
tech.root: TermServ
ms.assetid: d8114126-f518-4a43-8f6e-900fe84052e5
ms.date: 12/05/2018
ms.keywords: DeleteTarget, DeleteTarget method [Remote Desktop Services], DeleteTarget method [Remote Desktop Services],ITsSbResourcePluginStore interface, DeleteTarget method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],DeleteTarget method, ITsSbResourcePluginStore.DeleteTarget, ITsSbResourcePluginStore::DeleteTarget, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],DeleteTarget method, ITsSbResourcePluginStoreEx::DeleteTarget, sbtsv/ITsSbResourcePluginStore::DeleteTarget, sbtsv/ITsSbResourcePluginStoreEx::DeleteTarget, termserv.itssbresourcepluginstore_deletetarget
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbResourcePluginStore::DeleteTarget
 - sbtsv/ITsSbResourcePluginStore::DeleteTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.DeleteTarget
 - ITsSbResourcePluginStoreEx.DeleteTarget
---

# ITsSbResourcePluginStore::DeleteTarget


## -description

 Deletes a target.

## -parameters

### -param targetName [in]

The name of the target.

### -param hostName [in]

The name of the computer that hosts the target.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>