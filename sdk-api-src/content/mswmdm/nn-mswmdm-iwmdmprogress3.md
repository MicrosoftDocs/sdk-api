---
UID: NN:mswmdm.IWMDMProgress3
title: IWMDMProgress3 (mswmdm.h)
description: The optional, application-implemented IWMDMProgress3 interface extends IWMDMProgress2 by providing additional input parameters to specify which event is being monitored, and to allow for context-specific information.Applications that implement this callback interface should provide an implementation for methods corresponding to IWMDMProgress and IWMDMProgress2 for backward compatibility, in addition to the new methods.
helpviewer_keywords: ["IWMDMProgress3","IWMDMProgress3 interface [windows Media Device Manager]","IWMDMProgress3 interface [windows Media Device Manager]","described","IWMDMProgress3Interface","mswmdm/IWMDMProgress3","wmdm.iwmdmprogress3"]
old-location: wmdm\iwmdmprogress3.htm
tech.root: WMDM
ms.assetid: fc3a7031-ac1b-45cf-889b-2d40d50b347d
ms.date: 12/05/2018
ms.keywords: IWMDMProgress3, IWMDMProgress3 interface [windows Media Device Manager], IWMDMProgress3 interface [windows Media Device Manager],described, IWMDMProgress3Interface, mswmdm/IWMDMProgress3, wmdm.iwmdmprogress3
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
 - IWMDMProgress3
 - mswmdm/IWMDMProgress3
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
 - IWMDMProgress3
---

# IWMDMProgress3 interface


## -description

The optional, application-implemented <b>IWMDMProgress3</b> interface extends <b>IWMDMProgress2</b> by providing additional input parameters to specify which event is being monitored, and to allow for context-specific information.

Applications that implement this callback interface should provide an implementation for methods corresponding to <b>IWMDMProgress</b> and <b>IWMDMProgress2</b> for backward compatibility, in addition to the new methods.

## -inheritance

The <b>IWMDMProgress3</b> interface inherits from <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a>. <b>IWMDMProgress3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2">IWMDMProgress2 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
