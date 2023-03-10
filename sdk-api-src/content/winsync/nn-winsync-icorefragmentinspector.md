---
UID: NN:winsync.ICoreFragmentInspector
title: ICoreFragmentInspector (winsync.h)
description: Enumerates the ICoreFragment objects that are contained in a knowledge object.
helpviewer_keywords: ["ICoreFragmentInspector","ICoreFragmentInspector interface [Windows Sync]","ICoreFragmentInspector interface [Windows Sync]","described","winsync.icorefragmentinspector","winsync/ICoreFragmentInspector"]
old-location: winsync\icorefragmentinspector.htm
tech.root: winsync
ms.assetid: 10c22b92-bda8-42f6-9fd6-58e77e5a18d4
ms.date: 12/05/2018
ms.keywords: ICoreFragmentInspector, ICoreFragmentInspector interface [Windows Sync], ICoreFragmentInspector interface [Windows Sync],described, winsync.icorefragmentinspector, winsync/ICoreFragmentInspector
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
 - ICoreFragmentInspector
 - winsync/ICoreFragmentInspector
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
 - ICoreFragmentInspector
---

# ICoreFragmentInspector interface


## -description

Enumerates the <b>ICoreFragment</b> objects that are contained in a knowledge object.

## -inheritance

The <b>ICoreFragmentInspector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICoreFragmentInspector</b> also has these types of members:

## -remarks

An <b>ICoreFragmentInspector</b> object can be obtained by calling <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-getinspector">ISyncKnowledge2::GetInspector</a> on a knowledge object.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
