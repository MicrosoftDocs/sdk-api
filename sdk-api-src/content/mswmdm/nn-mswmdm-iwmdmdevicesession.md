---
UID: NN:mswmdm.IWMDMDeviceSession
title: IWMDMDeviceSession (mswmdm.h)
description: The IWMDMDeviceSession interface improves the efficiency of device operations by bundling multiple operations into one session.
helpviewer_keywords: ["IWMDMDeviceSession","IWMDMDeviceSession interface [windows Media Device Manager]","IWMDMDeviceSession interface [windows Media Device Manager]","described","IWMDMDeviceSessionInterface","mswmdm/IWMDMDeviceSession","wmdm.iwmdmdevicesession"]
old-location: wmdm\iwmdmdevicesession.htm
tech.root: WMDM
ms.assetid: 37a57fbe-d0f8-44ee-b6c5-2c6a34e12f2b
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceSession, IWMDMDeviceSession interface [windows Media Device Manager], IWMDMDeviceSession interface [windows Media Device Manager],described, IWMDMDeviceSessionInterface, mswmdm/IWMDMDeviceSession, wmdm.iwmdmdevicesession
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
 - IWMDMDeviceSession
 - mswmdm/IWMDMDeviceSession
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
 - IWMDMDeviceSession
---

# IWMDMDeviceSession interface


## -description

The <b>IWMDMDeviceSession</b> interface improves the efficiency of device operations by bundling multiple operations into one session. Using a single session allows Windows Media Device Manager to handle various operations, such as acquiring a device certificate, once over several operations.

## -inheritance

The <b>IWMDMDeviceSession</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMDeviceSession</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
