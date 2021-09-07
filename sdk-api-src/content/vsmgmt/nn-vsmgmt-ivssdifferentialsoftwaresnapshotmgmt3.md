---
UID: NN:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt3
title: IVssDifferentialSoftwareSnapshotMgmt3 (vsmgmt.h)
description: Defines methods that allow applications to use the shadow copy protection feature of VSS.
helpviewer_keywords: ["IVssDifferentialSoftwareSnapshotMgmt3","IVssDifferentialSoftwareSnapshotMgmt3 interface","IVssDifferentialSoftwareSnapshotMgmt3 interface","described","base.ivssdifferentialsoftwaresnapshotmgmt3","vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3"]
old-location: base\ivssdifferentialsoftwaresnapshotmgmt3.htm
tech.root: base
ms.assetid: e5abcf69-748a-4ed6-973d-8ba49ec22ef2
ms.date: 12/05/2018
ms.keywords: IVssDifferentialSoftwareSnapshotMgmt3, IVssDifferentialSoftwareSnapshotMgmt3 interface, IVssDifferentialSoftwareSnapshotMgmt3 interface,described, base.ivssdifferentialsoftwaresnapshotmgmt3, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVssDifferentialSoftwareSnapshotMgmt3
 - vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3
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
 - IVssDifferentialSoftwareSnapshotMgmt3
---

# IVssDifferentialSoftwareSnapshotMgmt3 interface


## -description

Defines methods that allow applications to use the shadow copy protection feature of VSS.

To obtain an instance of the <b>IVssDifferentialSoftwareSnapshotMgmt3</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a> interface and pass 
   the <b>IID_IVssDifferentialSoftwareSnapshotMgmt3</b> constant as the interface identifier (IID) parameter.

## -inheritance

The <b>IVssDifferentialSoftwareSnapshotMgmt3</b> interface inherits from <a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2">IVssDifferentialSoftwareSnapshotMgmt2</a> and <a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>. <b>IVssDifferentialSoftwareSnapshotMgmt3</b> also has these types of members:

## -remarks

An application with administrator privilege can use the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-setvolumeprotectlevel">SetVolumeProtectLevel</a> method to specify a shadow copy protection level for a volume and the separate volume that contains its shadow copy storage area. The same protection level should be set for both volumes. The possible protection levels are defined by the <a href="/windows/desktop/api/vsmgmt/ne-vsmgmt-vss_protection_level">VSS_PROTECTION_LEVEL</a> enumeration.

When a volume protection fault occurs, the application must call the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-getvolumeprotectlevel">GetVolumeProtectLevel</a> method for the volume to identify the cause of the fault.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>



<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2">IVssDifferentialSoftwareSnapshotMgmt2</a>
