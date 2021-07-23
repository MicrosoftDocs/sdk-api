---
UID: NF:vsmgmt.IVssSnapshotMgmt.GetProviderMgmtInterface
title: IVssSnapshotMgmt::GetProviderMgmtInterface (vsmgmt.h)
description: Returns an interface to further configure the system provider.
helpviewer_keywords: ["GetProviderMgmtInterface","GetProviderMgmtInterface method [VSS]","GetProviderMgmtInterface method [VSS]","IVssSnapshotMgmt interface","IVssSnapshotMgmt interface [VSS]","GetProviderMgmtInterface method","IVssSnapshotMgmt.GetProviderMgmtInterface","IVssSnapshotMgmt::GetProviderMgmtInterface","base.ivsssnapshotmgmt_getprovidermgmtinterface","vsmgmt/IVssSnapshotMgmt::GetProviderMgmtInterface"]
old-location: base\ivsssnapshotmgmt_getprovidermgmtinterface.htm
tech.root: base
ms.assetid: 814c6e2c-a5f8-4f44-b508-3a2e95bb1c54
ms.date: 12/05/2018
ms.keywords: GetProviderMgmtInterface, GetProviderMgmtInterface method [VSS], GetProviderMgmtInterface method [VSS],IVssSnapshotMgmt interface, IVssSnapshotMgmt interface [VSS],GetProviderMgmtInterface method, IVssSnapshotMgmt.GetProviderMgmtInterface, IVssSnapshotMgmt::GetProviderMgmtInterface, base.ivsssnapshotmgmt_getprovidermgmtinterface, vsmgmt/IVssSnapshotMgmt::GetProviderMgmtInterface
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
 - IVssSnapshotMgmt::GetProviderMgmtInterface
 - vsmgmt/IVssSnapshotMgmt::GetProviderMgmtInterface
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
 - IVssSnapshotMgmt.GetProviderMgmtInterface
---

# IVssSnapshotMgmt::GetProviderMgmtInterface


## -description

The 
    <b>GetProviderMgmtInterface</b> 
    method returns an interface to further configure the system provider.

## -parameters

### -param ProviderId [in]

This must be the system provider. The  <b>VSS_ID</b> for the system provider <code>{b5946137-7b9f-4925-af80-51abd60b20d5}</code>.

### -param InterfaceId [in]

Must be <b>IID_IVssDifferentialSoftwareSnapshotMgmt</b>, which represents the 
      <a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a> 
      interface.

### -param ppItf [out]

Address of an interface pointer that is filled in with the returned interface pointer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>



<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivsssnapshotmgmt">IVssSnapshotMgmt</a>