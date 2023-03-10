---
UID: NF:mswmdm.IMDSPDevice.SendOpaqueCommand
title: IMDSPDevice::SendOpaqueCommand (mswmdm.h)
description: The SendOpaqueCommand method sends a command through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.
helpviewer_keywords: ["IMDSPDevice interface [windows Media Device Manager]","SendOpaqueCommand method","IMDSPDevice.SendOpaqueCommand","IMDSPDevice::SendOpaqueCommand","IMDSPDeviceSendOpaqueCommand","SendOpaqueCommand","SendOpaqueCommand method [windows Media Device Manager]","SendOpaqueCommand method [windows Media Device Manager]","IMDSPDevice interface","mswmdm/IMDSPDevice::SendOpaqueCommand","wmdm.imdspdevice_sendopaquecommand"]
old-location: wmdm\imdspdevice_sendopaquecommand.htm
tech.root: WMDM
ms.assetid: d7b60187-84d1-4ff3-ab58-e6b8ea75ee37
ms.date: 12/05/2018
ms.keywords: IMDSPDevice interface [windows Media Device Manager],SendOpaqueCommand method, IMDSPDevice.SendOpaqueCommand, IMDSPDevice::SendOpaqueCommand, IMDSPDeviceSendOpaqueCommand, SendOpaqueCommand, SendOpaqueCommand method [windows Media Device Manager], SendOpaqueCommand method [windows Media Device Manager],IMDSPDevice interface, mswmdm/IMDSPDevice::SendOpaqueCommand, wmdm.imdspdevice_sendopaquecommand
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
 - IMDSPDevice::SendOpaqueCommand
 - mswmdm/IMDSPDevice::SendOpaqueCommand
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
 - IMDSPDevice.SendOpaqueCommand
---

# IMDSPDevice::SendOpaqueCommand


## -description

The <b>SendOpaqueCommand</b> method sends a command through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.

## -parameters

### -param pCommand [in, out]

Pointer to an <a href="/windows/desktop/WMDM/opaquecommand">OPAQUECOMMAND</a> structure containing the information required to execute the command.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is used with device commands that do not affect Windows Media Device Manager, and are passed through unchanged. A more efficient way to call commands on a device is to call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol">IMDSPDevice3::DeviceIoControl</a>.

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>