---
UID: NN:vsmgmt.IVssEnumMgmtObject
title: IVssEnumMgmtObject (vsmgmt.h)
description: Contains methods to iterate over and perform other operations on a list of enumerated objects. (IVssEnumMgmtObject)
helpviewer_keywords: ["IVssEnumMgmtObject","IVssEnumMgmtObject interface [Files]","IVssEnumMgmtObject interface [Files]","described","base.ivssenummgmtobject","vsmgmt/IVssEnumMgmtObject"]
old-location: base\ivssenummgmtobject.htm
tech.root: base
ms.assetid: c2067822-1824-4676-8376-7d83fcbbaea3
ms.date: 12/05/2018
ms.keywords: IVssEnumMgmtObject, IVssEnumMgmtObject interface [Files], IVssEnumMgmtObject interface [Files],described, base.ivssenummgmtobject, vsmgmt/IVssEnumMgmtObject
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVssEnumMgmtObject
 - vsmgmt/IVssEnumMgmtObject
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
 - IVssEnumMgmtObject
---

# IVssEnumMgmtObject interface


## -description

The <b>IVssEnumMgmtObject</b> interface contains 
    methods to iterate over and perform other operations on a list of enumerated objects.

The calling application is responsible for calling 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources held by the 
    returned <b>IVssEnumMgmtObject</b> when it is no longer 
    needed. It may also need to call <b>IUnknown::Release</b> to 
    release temporary objects (such as strings) returned during enumeration.

The 
    <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforsnapshot">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot</a>, 
    <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForVolume</a>, 
    <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasonvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasOnVolume</a>, and 
    <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-queryvolumessupportedfordiffareas">IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas</a> 
    methods return an <b>IVssEnumMgmtObject</b> object.

## -inheritance

The <b>IVssEnumMgmtObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssEnumMgmtObject</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforsnapshot">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot</a>



<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForVolume</a>



<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasonvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasOnVolume</a>



<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-queryvolumessupportedfordiffareas">IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
