---
UID: NN:winsync.ISyncKnowledge
title: ISyncKnowledge (winsync.h)
description: Represents knowledge that a replica has about its item store.
helpviewer_keywords: ["ISyncKnowledge","ISyncKnowledge interface [Windows Sync]","ISyncKnowledge interface [Windows Sync]","described","winsync.isyncknowledge","winsync/ISyncKnowledge"]
old-location: winsync\isyncknowledge.htm
tech.root: winsync
ms.assetid: cfb08476-7b5d-4953-b723-5160330e57be
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge, ISyncKnowledge interface [Windows Sync], ISyncKnowledge interface [Windows Sync],described, winsync.isyncknowledge, winsync/ISyncKnowledge
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
 - ISyncKnowledge
 - winsync/ISyncKnowledge
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
 - ISyncKnowledge
---

# ISyncKnowledge interface


## -description

Represents knowledge that a replica has about its item store.

## -inheritance

The <b>ISyncKnowledge</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncKnowledge</b> also has these types of members:

## -remarks

Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from knowledge inspection methods, such as <b>GetScopeVector</b>, <b>GetRangeExceptions</b>, <b>GetSingleItemExceptions</b>, <b>GetChangeUnitExceptions</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitexception">IChangeUnitException Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irangeexception">IRangeException Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ireplicakeymap">IReplicaKeyMap Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isingleitemexception">ISingleItemException Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
