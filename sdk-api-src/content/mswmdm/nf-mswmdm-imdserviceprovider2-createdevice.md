---
UID: NF:mswmdm.IMDServiceProvider2.CreateDevice
title: IMDServiceProvider2::CreateDevice (mswmdm.h)
description: The CreateDevice method is called by the Windows Media Device Manager to get the IMDSPDevice object(s) corresponding to the canonical device obtained from the PnP subsystem.
helpviewer_keywords: ["CreateDevice","CreateDevice method [windows Media Device Manager]","CreateDevice method [windows Media Device Manager]","IMDServiceProvider2 interface","IMDServiceProvider2 interface [windows Media Device Manager]","CreateDevice method","IMDServiceProvider2.CreateDevice","IMDServiceProvider2::CreateDevice","IMDServiceProvider2GetDevicesFromDevicePath","mswmdm/IMDServiceProvider2::CreateDevice","wmdm.imdserviceprovider2_createdevice"]
old-location: wmdm\imdserviceprovider2_createdevice.htm
tech.root: WMDM
ms.assetid: f724ef14-c572-41ca-a56b-fde85d7620e0
ms.date: 12/05/2018
ms.keywords: CreateDevice, CreateDevice method [windows Media Device Manager], CreateDevice method [windows Media Device Manager],IMDServiceProvider2 interface, IMDServiceProvider2 interface [windows Media Device Manager],CreateDevice method, IMDServiceProvider2.CreateDevice, IMDServiceProvider2::CreateDevice, IMDServiceProvider2GetDevicesFromDevicePath, mswmdm/IMDServiceProvider2::CreateDevice, wmdm.imdserviceprovider2_createdevice
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDServiceProvider2::CreateDevice
 - mswmdm/IMDServiceProvider2::CreateDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDServiceProvider2.CreateDevice
---

# IMDServiceProvider2::CreateDevice


## -description

The <b>CreateDevice</b> method is called by the Windows Media Device Manager to get the <b>IMDSPDevice</b> object(s) corresponding to the canonical device obtained from the PnP subsystem. This method must be implemented for PnP and Windows Explorer support, but otherwise it is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -parameters

### -param pwszDevicePath [in]

Pointer to a wide-character null-terminated string containing the device path of the device detected by Windows Media Device Manager. This name is obtained from the PnP subsystem, and is the canonical name plus "$ <i>#</i> ", where <i>#</i> is an auto-incremented number. This name can be passed directly to functions such as <b>CreateFile</b> to gain access to the underlying kernel device object. The service provider should create a wrapper <b>IMDSPDevice</b> object(s) for this device.

### -param pdwCount [out]

Pointer to a <b>DWORD</b> containing the number of <b>IMDSPDevice</b> objects that are created.

### -param pppDeviceArray [out]

An array of <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> interfaces representing the devices. Typically, there is only one array element, but a service provider can create more than one <b>IMDSPDevice</b> object corresponding to a device path name if it creates an <b>IMDSPDevice</b> object for each top-level storage. This is subject to change in the future, and the count may be restricted to 1.

## -returns

If the method succeeds it returns S_OK. If the method fails, it returns the Windows Media Device Manager error codes.

## -remarks

Windows Media Device Manager calls this method when an application starts, or when a Plug and Play compliant device connects with the computer.

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices-service-provider">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2">IMDServiceProvider2 Interface</a>