---
UID: NN:cscobj.IEnumOfflineFilesItems
title: IEnumOfflineFilesItems (cscobj.h)
description: Represents a collection of IOfflineFilesItem interface pointers.
helpviewer_keywords: ["IEnumOfflineFilesItems","IEnumOfflineFilesItems interface [Offline Files]","IEnumOfflineFilesItems interface [Offline Files]","described","cscobj/IEnumOfflineFilesItems","of.ienumofflinefilesitems"]
old-location: of\ienumofflinefilesitems.htm
tech.root: of
ms.assetid: 9bb1fa14-74d2-4c6f-b8ba-47c6e78d7a4f
ms.date: 12/05/2018
ms.keywords: IEnumOfflineFilesItems, IEnumOfflineFilesItems interface [Offline Files], IEnumOfflineFilesItems interface [Offline Files],described, cscobj/IEnumOfflineFilesItems, of.ienumofflinefilesitems
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumOfflineFilesItems
 - cscobj/IEnumOfflineFilesItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IEnumOfflineFilesItems
---

# IEnumOfflineFilesItems interface


## -description

Represents a collection of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a> interface pointers.

## -inheritance

The <b>IEnumOfflineFilesItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumOfflineFilesItems</b> also has these types of members:

## -remarks

To obtain an instance of this interface, first obtain an instance of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a> using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an instance of one of the following interfaces:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>
</li>
<li>
<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesdirectoryitem">IOfflineFilesDirectoryItem</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>
</li>
<li>
<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesserveritem">IOfflineFilesServerItem</a>
</li>
<li>
<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesshareitem">IOfflineFilesShareItem</a>
</li>
</ul>
<div class="alert"><b>Note</b>  The <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a> interface is only valid for directory, server, and share items. If <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> is called for the <b>IOfflineFilesItemContainer</b> interface on a file item (an instance of the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfileitem">IOfflineFilesFileItem</a> interface), it will fail with <b>E_NOINTERFACE</b>.</div>
<div> </div>
For a code example that shows how to use the <b>IEnumOfflineFilesItems</b> interface, see <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemcontainer-enumitems">IOfflineFilesItemContainer::EnumItems</a>.

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
