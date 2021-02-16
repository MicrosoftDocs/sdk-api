---
UID: NF:portabledeviceapi.IPortableDeviceService.SendCommand
title: IPortableDeviceService::SendCommand (portabledeviceapi.h)
description: Sends a standard WPD command and its parameters to the service.
helpviewer_keywords: ["IPortableDeviceService interface [Windows Portable Devices SDK]","SendCommand method","IPortableDeviceService.SendCommand","IPortableDeviceService::SendCommand","SendCommand","SendCommand method [Windows Portable Devices SDK]","SendCommand method [Windows Portable Devices SDK]","IPortableDeviceService interface","portabledeviceapi/IPortableDeviceService::SendCommand","wpdsdk.iportabledeviceservice_sendcommand"]
old-location: wpdsdk\iportabledeviceservice_sendcommand.htm
tech.root: wpdsdk
ms.assetid: c6c42347-145c-4be7-bea6-34b13c211cb1
ms.date: 12/05/2018
ms.keywords: IPortableDeviceService interface [Windows Portable Devices SDK],SendCommand method, IPortableDeviceService.SendCommand, IPortableDeviceService::SendCommand, SendCommand, SendCommand method [Windows Portable Devices SDK], SendCommand method [Windows Portable Devices SDK],IPortableDeviceService interface, portabledeviceapi/IPortableDeviceService::SendCommand, wpdsdk.iportabledeviceservice_sendcommand
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
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
 - IPortableDeviceService::SendCommand
 - portabledeviceapi/IPortableDeviceService::SendCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService.SendCommand
---

# IPortableDeviceService::SendCommand


## -description

The <b>SendCommand</b> method sends a standard WPD command and its parameters to the service.

## -parameters

### -param dwFlags [in]

Not used.

### -param pParameters [in]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface specifying the command parameters.

### -param ppResults [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface specifying the command results.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

This method should only be used to send standard WPD commands to the service. To invoke service methods, use the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethods">IPortableDeviceServiceMethods</a> interface.

This method may fail even though it returns <b>S_OK</b> as its <b>HRESULT</b> value. To determine if a command succeeded, an application should always examine the properties referenced by the <i>ppResults</i> parameter:

<ul>
<li>The <a href="/windows/desktop/wpd_sdk/common-properties">WPD_PROPERTY_COMMON_HRESULT</a> property indicates if the command succeeded.</li>
<li>If the command failed, the <a href="/windows/desktop/wpd_sdk/common-properties">WPD_PROPERTY_COMMON_DRIVER_ERROR_CODE</a> property will contain driver-specific error codes.</li>
</ul>
The object referenced by the <i>pParameters</i> parameter must specify at least these properties:

<ul>
<li><a href="/windows/desktop/wpd_sdk/common-properties">WPD_PROPERTY_COMMON_COMMAND_CATEGORY</a>, which should contain a command category, such as the <b>fmtid</b> member of the <a href="/windows/desktop/wpd_sdk/wpd-command-common-reset-device-command">WPD_COMMAND_COMMON_RESET_DEVICE</a> property</li>
<li><a href="/windows/desktop/wpd_sdk/common-properties">WPD_PROPERTY_COMMON_COMMAND_ID</a>, which should contain a command identifier, such as the <b>pid</b> member of the  <a href="/windows/desktop/wpd_sdk/wpd-command-common-reset-device-command">WPD_COMMAND_COMMON_RESET_DEVICE</a> property.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>