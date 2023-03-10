---
UID: NN:mswmdm.IMDSPStorage3
title: IMDSPStorage3 (mswmdm.h)
description: The IMDSPStorage3 interface extends IMDSPStorage2 by supporting metadata.
helpviewer_keywords: ["IMDSPStorage3","IMDSPStorage3 interface [windows Media Device Manager]","IMDSPStorage3 interface [windows Media Device Manager]","described","IMDSPStorage3Interface","mswmdm/IMDSPStorage3","wmdm.imdspstorage3"]
old-location: wmdm\imdspstorage3.htm
tech.root: WMDM
ms.assetid: 5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919
ms.date: 12/05/2018
ms.keywords: IMDSPStorage3, IMDSPStorage3 interface [windows Media Device Manager], IMDSPStorage3 interface [windows Media Device Manager],described, IMDSPStorage3Interface, mswmdm/IMDSPStorage3, wmdm.imdspstorage3
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMDSPStorage3
 - mswmdm/IMDSPStorage3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IMDSPStorage3
---

# IMDSPStorage3 interface


## -description

The <b>IMDSPStorage3</b> interface extends <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2</a> by supporting metadata. This interface is optional. Service providers must implement this interface only if they are going to support metadata. If the device parameter <i>UseMetadataViews</i> is set to 1, this interface must be implemented and the <b>GetMetadata</b> method becomes mandatory, although <b>SetMetadata</b> is still optional. For more information, see <a href="/windows/desktop/WMDM/device-parameters">Device Parameters</a>.

## -inheritance

The <b>IMDSPStorage3</b> interface inherits from <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2</a>. <b>IMDSPStorage3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4">IMDSPStorage4 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
