---
UID: NN:vsmgmt.IVssSnapshotMgmt
title: IVssSnapshotMgmt (vsmgmt.h)
description: Provides a method that returns an interface to further configure a shadow copy provider.
helpviewer_keywords: ["IVssSnapshotMgmt","IVssSnapshotMgmt interface [Files]","IVssSnapshotMgmt interface [Files]","described","base.ivsssnapshotmgmt","vsmgmt/IVssSnapshotMgmt"]
old-location: base\ivsssnapshotmgmt.htm
tech.root: base
ms.assetid: 5e5694a1-7c17-4d8a-b094-09dcf28a636f
ms.date: 12/05/2018
ms.keywords: IVssSnapshotMgmt, IVssSnapshotMgmt interface [Files], IVssSnapshotMgmt interface [Files],described, base.ivsssnapshotmgmt, vsmgmt/IVssSnapshotMgmt
f1_keywords:
- vsmgmt/IVssSnapshotMgmt
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
- IVssSnapshotMgmt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssSnapshotMgmt interface


## -description


The <b>IVssSnapshotMgmt</b> interface provides a 
    method that returns an interface to further configure a shadow copy provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssSnapshotMgmt</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssSnapshotMgmt</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssSnapshotMgmt</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivsssnapshotmgmt-getprovidermgmtinterface">GetProviderMgmtInterface</a>
</td>
<td align="left" width="63%">
Returns an interface to further configure a shadow copy provider.</p> (Inherited from <b>IVssSnapshotMgmt</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivsssnapshotmgmt-querysnapshotsbyvolume">QuerySnapshotsByVolume</a>
</td>
<td align="left" width="63%">
Reserved for system use.</p> (Inherited from <b>IVssSnapshotMgmt</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivsssnapshotmgmt-queryvolumessupportedforsnapshots">QueryVolumesSupportedForSnapshots</a>
</td>
<td align="left" width="63%">
Reserved for system use.</p> (Inherited from <b>IVssSnapshotMgmt</b>)</td>
</tr>
</table> 


## -remarks



The <b>IVssSnapshotMgmt</b> interface can be invoked 
    remotely using DCOM. The caller must be a member of the local administrators group on the remote machine.


#### Examples


```cpp
#include "vss.h"
#include "vsmgmt.h"

void main()
{
    // software-provider id is {b5946137-7b9f-4925-af80-51abd60b20d5}
    const VSS_ID ProviderId = { 0xb5946137, 
                                0x7b9f, 
                                0x4925, 
                              { 0xaf,0x80,0x51,0xab,0xd6,0xb,0x20,0xd5 } };

    HRESULT                               hr        = S_OK;
    IVssSnapshotMgmt*                     pMgmt     = NULL;
    IVssDifferentialSoftwareSnapshotMgmt* pDiffMgmt = NULL;

    hr = CoCreateInstance(CLSID_VssSnapshotMgmt,
                          NULL,
                          CLSCTX_ALL,
                          IID_IVssSnapshotMgmt,
                          (void**)&(pMgmt));
    if (FAILED(hr)) 
    {
        // error handling code
    }

    hr = pMgmt->GetProviderMgmtInterface(ProviderId, 
                                         IID_IVssDifferentialSoftwareSnapshotMgmt, 
                                         (IUnknown**)&pDiffMgmt);
    if (FAILED(hr)) 
    {
        pMgmt->Release();
    }

    // processing code

    pDiffMgmt->Release();
    pMgmt->Release();
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
 

 

