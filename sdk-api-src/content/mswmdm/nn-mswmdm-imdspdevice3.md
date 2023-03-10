---
UID: NN:mswmdm.IMDSPDevice3
title: IMDSPDevice3 (mswmdm.h)
description: The IMDSPDevice3 interface must be supported for devices that expect to synchronize with Windows Media Player.
helpviewer_keywords: ["IMDSPDevice3","IMDSPDevice3 interface [windows Media Device Manager]","IMDSPDevice3 interface [windows Media Device Manager]","described","IMDSPDevice3Interface","mswmdm/IMDSPDevice3","wmdm.imdspdevice3"]
old-location: wmdm\imdspdevice3.htm
tech.root: WMDM
ms.assetid: 919c26f4-6954-462a-8b4a-530e78bb72e6
ms.date: 12/05/2018
ms.keywords: IMDSPDevice3, IMDSPDevice3 interface [windows Media Device Manager], IMDSPDevice3 interface [windows Media Device Manager],described, IMDSPDevice3Interface, mswmdm/IMDSPDevice3, wmdm.imdspdevice3
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
 - IMDSPDevice3
 - mswmdm/IMDSPDevice3
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
 - IMDSPDevice3
---

# IMDSPDevice3 interface


## -description

The <b>IMDSPDevice3</b> interface must be supported for devices that expect to synchronize with Windows Media Player. For more information, see <a href="/windows/desktop/WMDM/enabling-synchronization-with-windows-media-player">Enabling Synchronization with Windows Media Player</a>.

The <b>IMDSPDevice3</b> interface extends <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2</a> by providing ability to query properties and capabilities of the device with regard to an object format.

<div class="alert"><b>Note</b>  Unless the service provider has added the device parameter <i>UseExtendedWmdm</i> with a value of 1, Windows Media Device Manager will not call this interface. See <a href="/windows/desktop/WMDM/device-parameters">Device Parameters</a> for more information about this.</div>
<div> </div>

## -inheritance

The <b>IMDSPDevice3</b> interface inherits from <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2</a>. <b>IMDSPDevice3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
