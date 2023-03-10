---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.Cancel
title: ICreateDeviceAccessAsync::Cancel (deviceaccess.h)
description: The Cancel method attempts to cancel an asynchronous operation that is in progress.
helpviewer_keywords: ["Cancel","Cancel method [Device Access Broker API]","Cancel method [Device Access Broker API]","ICreateDeviceAccessAsync interface","ICreateDeviceAccessAsync interface [Device Access Broker API]","Cancel method","ICreateDeviceAccessAsync.Cancel","ICreateDeviceAccessAsync::Cancel","deviceaccess.icreatedeviceaccessasync_cancel","deviceaccess/ICreateDeviceAccessAsync::Cancel"]
old-location: deviceaccess\icreatedeviceaccessasync_cancel.htm
tech.root: deviceaccess
ms.assetid: 06e5af2d-8bd8-44b1-9ead-caa362284530
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Device Access Broker API], Cancel method [Device Access Broker API],ICreateDeviceAccessAsync interface, ICreateDeviceAccessAsync interface [Device Access Broker API],Cancel method, ICreateDeviceAccessAsync.Cancel, ICreateDeviceAccessAsync::Cancel, deviceaccess.icreatedeviceaccessasync_cancel, deviceaccess/ICreateDeviceAccessAsync::Cancel
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
 - ICreateDeviceAccessAsync::Cancel
 - deviceaccess/ICreateDeviceAccessAsync::Cancel
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
 - ICreateDeviceAccessAsync.Cancel
---

# ICreateDeviceAccessAsync::Cancel


## -description

The <b>Cancel</b> method attempts to cancel an asynchronous operation that is in progress.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the operation is successfully canceled, a call to the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult">GetResult</a> method occurs.

Your application can call  <b>Cancel</b> at any time. If the operation is already closed or completed, it has no effect.

## -see-also

<a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-icreatedeviceaccessasync">ICreateDeviceAccessAsync</a>
