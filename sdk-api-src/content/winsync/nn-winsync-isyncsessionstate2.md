---
UID: NN:winsync.ISyncSessionState2
title: ISyncSessionState2 (winsync.h)
description: Represents additional information about the current synchronization session.
helpviewer_keywords: ["ISyncSessionState2","ISyncSessionState2 interface [Windows Sync]","ISyncSessionState2 interface [Windows Sync]","described","winsync.isyncsessionstate2","winsync/ISyncSessionState2"]
old-location: winsync\isyncsessionstate2.htm
tech.root: winsync
ms.assetid: c98e675f-48f4-4ffa-bc81-18a58edd8c34
ms.date: 12/05/2018
ms.keywords: ISyncSessionState2, ISyncSessionState2 interface [Windows Sync], ISyncSessionState2 interface [Windows Sync],described, winsync.isyncsessionstate2, winsync/ISyncSessionState2
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
 - ISyncSessionState2
 - winsync/ISyncSessionState2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsync.h
api_name:
 - ISyncSessionState2
---

# ISyncSessionState2 interface


## -description

Represents additional information about the current synchronization session.

## -inheritance

The <b>ISyncSessionState2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState</a>. <b>ISyncSessionState2</b> also has these types of members:

## -remarks

An <b>ISyncSessionState2</b> object can be obtained by passing <b>IID_ISyncSessionState2</b> to the <b>QueryInterface</b> method of an <b>ISyncSessionState</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
