---
UID: NF:mswmdm.IMDSPDevice.GetVersion
title: IMDSPDevice::GetVersion (mswmdm.h)
description: The GetVersion method retrieves the version number of the device.
helpviewer_keywords: ["GetVersion","GetVersion method [windows Media Device Manager]","GetVersion method [windows Media Device Manager]","IMDSPDevice interface","IMDSPDevice interface [windows Media Device Manager]","GetVersion method","IMDSPDevice.GetVersion","IMDSPDevice::GetVersion","IMDSPDeviceGetVersion","mswmdm/IMDSPDevice::GetVersion","wmdm.imdspdevice_getversion"]
old-location: wmdm\imdspdevice_getversion.htm
tech.root: WMDM
ms.assetid: 88c935ad-dbf0-41bb-8676-ddafe9d1fe0e
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [windows Media Device Manager], GetVersion method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetVersion method, IMDSPDevice.GetVersion, IMDSPDevice::GetVersion, IMDSPDeviceGetVersion, mswmdm/IMDSPDevice::GetVersion, wmdm.imdspdevice_getversion
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
 - IMDSPDevice::GetVersion
 - mswmdm/IMDSPDevice::GetVersion
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
 - IMDSPDevice.GetVersion
---

# IMDSPDevice::GetVersion


## -description

The <b>GetVersion</b> method retrieves the version number of the device.

## -parameters

### -param pdwVersion [out]

Pointer to a <b>DWORD</b> to receive the version number of the device.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>