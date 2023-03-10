---
UID: NF:mswmdm.IMDSPDevice.GetName
title: IMDSPDevice::GetName (mswmdm.h)
description: The GetName method retrieves the name of the device.
helpviewer_keywords: ["GetName","GetName method [windows Media Device Manager]","GetName method [windows Media Device Manager]","IMDSPDevice interface","IMDSPDevice interface [windows Media Device Manager]","GetName method","IMDSPDevice.GetName","IMDSPDevice::GetName","IMDSPDeviceGetName","mswmdm/IMDSPDevice::GetName","wmdm.imdspdevice_getname"]
old-location: wmdm\imdspdevice_getname.htm
tech.root: WMDM
ms.assetid: bc4fef6e-8faf-4114-a68d-bbc30bc18130
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [windows Media Device Manager], GetName method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetName method, IMDSPDevice.GetName, IMDSPDevice::GetName, IMDSPDeviceGetName, mswmdm/IMDSPDevice::GetName, wmdm.imdspdevice_getname
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
 - IMDSPDevice::GetName
 - mswmdm/IMDSPDevice::GetName
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
 - IMDSPDevice.GetName
---

# IMDSPDevice::GetName


## -description

The <b>GetName</b> method retrieves the name of the device.

## -parameters

### -param pwszName [out]

Pointer to an array of 16-bit Unicode characters that receives the device name string.

### -param nMaxChars [in]

Maximum number of characters to copy to the string.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The <b>LPWSTR</b> string type is a 16-bit Unicode character string and does not accept byte-sized characters. To convert a string of byte-sized characters (<b>LPCSTR</b>) to an <b>LPWSTR</b> string, use the <b>MultiByteToWideChar</b> function as described in Microsoft Windows documentation.

Device names must not contain trailing spaces.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-gettype">IMDSPDevice::GetType</a>