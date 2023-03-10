---
UID: NN:winsync.ISyncFilterInfo
title: ISyncFilterInfo (winsync.h)
description: Represents information about a filter that is used to control the data that is included in an ISyncChangeBatch object.
helpviewer_keywords: ["ISyncFilterInfo","ISyncFilterInfo interface [Windows Sync]","ISyncFilterInfo interface [Windows Sync]","described","winsync.isyncfilterinfo","winsync/ISyncFilterInfo"]
old-location: winsync\isyncfilterinfo.htm
tech.root: winsync
ms.assetid: 89a6d1c4-691d-4356-9ef5-1364b5a7507d
ms.date: 12/05/2018
ms.keywords: ISyncFilterInfo, ISyncFilterInfo interface [Windows Sync], ISyncFilterInfo interface [Windows Sync],described, winsync.isyncfilterinfo, winsync/ISyncFilterInfo
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
 - ISyncFilterInfo
 - winsync/ISyncFilterInfo
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
 - ISyncFilterInfo
---

# ISyncFilterInfo interface


## -description

Represents information about a filter that is used to control the data that is included in an <b>ISyncChangeBatch</b> object.

## -inheritance

The <b>ISyncFilterInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncFilterInfo</b> also has these types of members:

## -remarks

If a provider filters the contents of a change batch that it creates, it must create a filtered <b>ISyncChangeBatch</b> object.  The filtered change batch object contains an <b>ISyncFilterInfo</b> object that describes how the contents of the change batch were filtered.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
