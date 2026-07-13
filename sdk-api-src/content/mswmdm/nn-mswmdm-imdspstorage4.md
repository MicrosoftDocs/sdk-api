---
UID: NN:mswmdm.IMDSPStorage4
title: IMDSPStorage4 (mswmdm.h)
description: The IMDSPStorage4 interface extends IMDSPStorage3 for supporting virtual storages (such as playlists and albums) and metadata.Note  Unless the service provider has added the device parameter UseExtendedWmdm with a value of 1, Windows Media Device Manager will not call this interface. See Device Parameters for more information about this. .
helpviewer_keywords: ["IMDSPStorage4","IMDSPStorage4 interface [windows Media Device Manager]","IMDSPStorage4 interface [windows Media Device Manager]","described","IMDSPStorage4Interface","mswmdm/IMDSPStorage4","wmdm.imdspstorage4"]
old-location: wmdm\imdspstorage4.htm
tech.root: WMDM
ms.assetid: c1236acc-1f11-4501-9374-2486f7d61db3
ms.date: 12/05/2018
ms.keywords: IMDSPStorage4, IMDSPStorage4 interface [windows Media Device Manager], IMDSPStorage4 interface [windows Media Device Manager],described, IMDSPStorage4Interface, mswmdm/IMDSPStorage4, wmdm.imdspstorage4
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
 - IMDSPStorage4
 - mswmdm/IMDSPStorage4
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
 - IMDSPStorage4
---

# IMDSPStorage4 interface


## -description

The <b>IMDSPStorage4</b> interface extends <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3">IMDSPStorage3</a> for supporting virtual storages (such as playlists and albums) and metadata.

<div class="alert"><b>Note</b>  Unless the service provider has added the device parameter <b>UseExtendedWmdm</b> with a value of 1, Windows Media Device Manager will not call this interface. See <a href="/windows/desktop/WMDM/device-parameters">Device Parameters</a> for more information about this.</div>
<div> </div>

## -inheritance

The <b>IMDSPStorage4</b> interface inherits from <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3">IMDSPStorage3</a>. <b>IMDSPStorage4</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3">IMDSPStorage3 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
