---
UID: NN:vsmgmt.IVssSnapshotMgmt2
title: IVssSnapshotMgmt2 (vsmgmt.h)
description: Provides a method to retrieve the minimum size of the shadow copy storage area.
helpviewer_keywords: ["IVssSnapshotMgmt2","IVssSnapshotMgmt2 interface [Files]","IVssSnapshotMgmt2 interface [Files]","described","base.ivsssnapshotmgmt2","vsmgmt/IVssSnapshotMgmt2"]
old-location: base\ivsssnapshotmgmt2.htm
tech.root: base
ms.assetid: 92c8c960-d548-4a44-8b10-b6180c974473
ms.date: 12/05/2018
ms.keywords: IVssSnapshotMgmt2, IVssSnapshotMgmt2 interface [Files], IVssSnapshotMgmt2 interface [Files],described, base.ivsssnapshotmgmt2, vsmgmt/IVssSnapshotMgmt2
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IVssSnapshotMgmt2
 - vsmgmt/IVssSnapshotMgmt2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssSnapshotMgmt2
---

# IVssSnapshotMgmt2 interface


## -description

The <b>IVssSnapshotMgmt2</b> interface 
    provides a method to retrieve the minimum size of the shadow copy storage area.

## -inheritance

The <b>IVssSnapshotMgmt2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssSnapshotMgmt2</b> also has these types of members:

## -remarks

To obtain an instance of the <b>IVssSnapshotMgmt2</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivsssnapshotmgmt">IVssSnapshotMgmt</a> interface, passing 
   <b>IID_IVssSnapshotMgmt2</b> as the <i>riid</i> parameter.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
