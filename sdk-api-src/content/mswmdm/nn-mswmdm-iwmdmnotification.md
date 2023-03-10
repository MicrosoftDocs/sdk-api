---
UID: NN:mswmdm.IWMDMNotification
title: IWMDMNotification (mswmdm.h)
description: The optional, application-implemented IWMDMNotification interface allows applications and service providers to receive notifications when either devices or memory storages (such as RAM cards) are connected or disconnected from the computer.Note  This method will be called only for registered Plug and Play devices. Other device arrivals or departures will not cause this interface to be called. This interface GUID is not properly defined in mssachlp.lib; therefore, you must
helpviewer_keywords: ["IWMDMNotification","IWMDMNotification interface [windows Media Device Manager]","IWMDMNotification interface [windows Media Device Manager]","described","IWMDMNotificationInterface","mswmdm/IWMDMNotification","wmdm.iwmdmnotification"]
old-location: wmdm\iwmdmnotification.htm
tech.root: WMDM
ms.assetid: 3089a04d-24f5-4a4c-9df5-b4073fef358a
ms.date: 12/05/2018
ms.keywords: IWMDMNotification, IWMDMNotification interface [windows Media Device Manager], IWMDMNotification interface [windows Media Device Manager],described, IWMDMNotificationInterface, mswmdm/IWMDMNotification, wmdm.iwmdmnotification
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
 - IWMDMNotification
 - mswmdm/IWMDMNotification
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
 - IWMDMNotification
---

# IWMDMNotification interface


## -description

The optional, application-implemented <b>IWMDMNotification</b> interface allows applications and service providers to receive notifications when either devices or memory storages (such as RAM cards) are connected or disconnected from the computer.

<div class="alert"><b>Note</b>  This method will be called only for registered Plug and Play devices. Other device arrivals or departures will not cause this interface to be called.</div>
<div> </div>
This interface GUID is not properly defined in mssachlp.lib; therefore, you must #include both mswmdm.h and mswmdm_i.c (from wmdm.idl) if implementing this interface, to get the proper definitions.

## -inheritance

The <b>IWMDMNotification</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMNotification</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
