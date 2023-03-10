---
UID: NN:deviceaccess.ICreateDeviceAccessAsync
title: ICreateDeviceAccessAsync (deviceaccess.h)
description: The ICreateDeviceAccessAsync interface is returned from a call to CreateDeviceAccessInstance.
helpviewer_keywords: ["ICreateDeviceAccessAsync","ICreateDeviceAccessAsync interface [Device Access Broker API]","ICreateDeviceAccessAsync interface [Device Access Broker API]","described","deviceaccess.icreatedeviceaccessasync","deviceaccess/ICreateDeviceAccessAsync"]
old-location: deviceaccess\icreatedeviceaccessasync.htm
tech.root: deviceaccess
ms.assetid: ebc8d694-c933-4d98-95f5-67b0dd733d4d
ms.date: 12/05/2018
ms.keywords: ICreateDeviceAccessAsync, ICreateDeviceAccessAsync interface [Device Access Broker API], ICreateDeviceAccessAsync interface [Device Access Broker API],described, deviceaccess.icreatedeviceaccessasync, deviceaccess/ICreateDeviceAccessAsync
req.header: deviceaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Deviceaccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Deviceaccess.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICreateDeviceAccessAsync
 - deviceaccess/ICreateDeviceAccessAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Deviceaccess.lib
 - Deviceaccess.dll
api_name:
 - ICreateDeviceAccessAsync
---

# ICreateDeviceAccessAsync interface


## -description

The <b>ICreateDeviceAccessAsync</b> interface is returned from a call to CreateDeviceAccessInstance. It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.

## -inheritance

The <b>ICreateDeviceAccessAsync</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateDeviceAccessAsync</b> also has these types of members:

