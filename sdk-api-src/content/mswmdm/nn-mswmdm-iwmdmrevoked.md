---
UID: NN:mswmdm.IWMDMRevoked
title: IWMDMRevoked (mswmdm.h)
description: The IWMDMRevoked interface retrieves the URL from which updated components can be downloaded, if a transfer fails with a revocation error.
helpviewer_keywords: ["IWMDMRevoked","IWMDMRevoked interface [windows Media Device Manager]","IWMDMRevoked interface [windows Media Device Manager]","described","IWMDMRevokedInterface","mswmdm/IWMDMRevoked","wmdm.iwmdmrevoked"]
old-location: wmdm\iwmdmrevoked.htm
tech.root: WMDM
ms.assetid: b627f243-3652-4db9-8a5e-6a2146b73424
ms.date: 12/05/2018
ms.keywords: IWMDMRevoked, IWMDMRevoked interface [windows Media Device Manager], IWMDMRevoked interface [windows Media Device Manager],described, IWMDMRevokedInterface, mswmdm/IWMDMRevoked, wmdm.iwmdmrevoked
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
 - IWMDMRevoked
 - mswmdm/IWMDMRevoked
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
 - IWMDMRevoked
---

# IWMDMRevoked interface


## -description

The <b>IWMDMRevoked</b> interface retrieves the URL from which updated components can be downloaded, if a transfer fails with a revocation error. The secured content provider determines whether or not to allow a transfer, based on the application certificates of the components involved. You can access the <b>IWMDMRevoked</b> interface by calling <b>QueryInterface</b> on the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl</a> interface.

## -inheritance

The <b>IWMDMRevoked</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMRevoked</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
