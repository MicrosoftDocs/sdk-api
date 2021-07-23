---
UID: NN:winsync.IChangeUnitListFilterInfo
title: IChangeUnitListFilterInfo (winsync.h)
description: Represents a filter that can be used to control which change units are included for items in an ISyncChangeBatch object.
helpviewer_keywords: ["IChangeUnitListFilterInfo","IChangeUnitListFilterInfo interface [Windows Sync]","IChangeUnitListFilterInfo interface [Windows Sync]","described","winsync.ichangeunitlistfilterinfo","winsync/IChangeUnitListFilterInfo"]
old-location: winsync\ichangeunitlistfilterinfo.htm
tech.root: winsync
ms.assetid: fd379fc6-22e5-4165-b4e6-480bc65cccb3
ms.date: 12/05/2018
ms.keywords: IChangeUnitListFilterInfo, IChangeUnitListFilterInfo interface [Windows Sync], IChangeUnitListFilterInfo interface [Windows Sync],described, winsync.ichangeunitlistfilterinfo, winsync/IChangeUnitListFilterInfo
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
 - IChangeUnitListFilterInfo
 - winsync/IChangeUnitListFilterInfo
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
 - IChangeUnitListFilterInfo
---

# IChangeUnitListFilterInfo interface


## -description

Represents a filter that can be used to control which change units are included for items in an <b>ISyncChangeBatch</b> object.

## -inheritance

The <b>IChangeUnitListFilterInfo</b> interface inherits from <b>ISyncFilterInfo</b>. <b>IChangeUnitListFilterInfo</b> also has these types of members:

## -remarks

If a provider filters the contents of a change batch that it creates, it must create a filtered <b>ISyncChangeBatch</b> object instead of a standard change batch object. The filtered change batch object contains an <b>IChangeUnitListFilterInfo</b> object that describes how the contents of the change batch were filtered.

## -see-also

<b>ISyncFilterInfo</b>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
