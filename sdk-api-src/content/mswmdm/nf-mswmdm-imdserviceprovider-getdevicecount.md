---
UID: NF:mswmdm.IMDServiceProvider.GetDeviceCount
title: IMDServiceProvider::GetDeviceCount (mswmdm.h)
description: The GetDeviceCount method returns the number of installed physical or software devices that are currently attached and are known by the service provider.
helpviewer_keywords: ["GetDeviceCount","GetDeviceCount method [windows Media Device Manager]","GetDeviceCount method [windows Media Device Manager]","IMDServiceProvider interface","IMDServiceProvider interface [windows Media Device Manager]","GetDeviceCount method","IMDServiceProvider.GetDeviceCount","IMDServiceProvider::GetDeviceCount","IMDServiceProviderGetDeviceCount","mswmdm/IMDServiceProvider::GetDeviceCount","wmdm.imdserviceprovider_getdevicecount"]
old-location: wmdm\imdserviceprovider_getdevicecount.htm
tech.root: WMDM
ms.assetid: 9cca4cb7-f569-452f-92dc-409b996ede17
ms.date: 12/05/2018
ms.keywords: GetDeviceCount, GetDeviceCount method [windows Media Device Manager], GetDeviceCount method [windows Media Device Manager],IMDServiceProvider interface, IMDServiceProvider interface [windows Media Device Manager],GetDeviceCount method, IMDServiceProvider.GetDeviceCount, IMDServiceProvider::GetDeviceCount, IMDServiceProviderGetDeviceCount, mswmdm/IMDServiceProvider::GetDeviceCount, wmdm.imdserviceprovider_getdevicecount
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
 - IMDServiceProvider::GetDeviceCount
 - mswmdm/IMDServiceProvider::GetDeviceCount
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
 - IMDServiceProvider.GetDeviceCount
---

# IMDServiceProvider::GetDeviceCount


## -description

The <b>GetDeviceCount</b> method returns the number of installed physical or software devices that are currently attached and are known by the service provider.

## -parameters

### -param pdwCount [out]

Pointer to a <b>DWORD</b> containing the count of known devices.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The service provider should return only the number of supported devices that are currently attached to the computer.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider">IMDServiceProvider Interface</a>