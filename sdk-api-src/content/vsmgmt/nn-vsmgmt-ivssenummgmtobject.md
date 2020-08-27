---
UID: NN:vsmgmt.IVssEnumMgmtObject
title: IVssEnumMgmtObject (vsmgmt.h)
description: Contains methods to iterate over and perform other operations on a list of enumerated objects.
helpviewer_keywords: ["IVssEnumMgmtObject","IVssEnumMgmtObject interface [Files]","IVssEnumMgmtObject interface [Files]","described","base.ivssenummgmtobject","vsmgmt/IVssEnumMgmtObject"]
old-location: base\ivssenummgmtobject.htm
tech.root: base
ms.assetid: c2067822-1824-4676-8376-7d83fcbbaea3
ms.date: 12/05/2018
ms.keywords: IVssEnumMgmtObject, IVssEnumMgmtObject interface [Files], IVssEnumMgmtObject interface [Files],described, base.ivssenummgmtobject, vsmgmt/IVssEnumMgmtObject
f1_keywords:
- vsmgmt/IVssEnumMgmtObject
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VsMgmt.h
api_name:
- IVssEnumMgmtObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssEnumMgmtObject interface


## -description


The <b>IVssEnumMgmtObject</b> interface contains 
    methods to iterate over and perform other operations on a list of enumerated objects.

The calling application is responsible for calling 
    <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources held by the 
    returned <b>IVssEnumMgmtObject</b> when it is no longer 
    needed. It may also need to call <b>IUnknown::Release</b> to 
    release temporary objects (such as strings) returned during enumeration.

The 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforsnapshot">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForVolume</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasonvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasOnVolume</a>, and 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-queryvolumessupportedfordiffareas">IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas</a> 
    methods return an <b>IVssEnumMgmtObject</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssEnumMgmtObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssEnumMgmtObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssEnumMgmtObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssenummgmtobject-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the specified list of enumerated elements by creating a copy of the 
    <b>IVssEnumMgmtObject</b> enumerator object.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssenummgmtobject-next">Next</a>
</td>
<td align="left" width="63%">
Returns the specified number of objects from the specified list of enumerated 
     objects.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssenummgmtobject-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator so that 
     <b>IVssEnumMgmtObject</b> starts at the first enumerated 
     object.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssenummgmtobject-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of objects.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforsnapshot">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasforvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForVolume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-querydiffareasonvolume">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasOnVolume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-queryvolumessupportedfordiffareas">IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas</a>



<a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
 

 

