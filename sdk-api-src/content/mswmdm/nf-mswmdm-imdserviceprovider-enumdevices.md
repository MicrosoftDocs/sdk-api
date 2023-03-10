---
UID: NF:mswmdm.IMDServiceProvider.EnumDevices
title: IMDServiceProvider::EnumDevices (mswmdm.h)
description: The EnumDevices method enumerates the installed physical or software devices that are currently attached and are known by the service provider.
helpviewer_keywords: ["EnumDevices","EnumDevices method [windows Media Device Manager]","EnumDevices method [windows Media Device Manager]","IMDServiceProvider interface","IMDServiceProvider interface [windows Media Device Manager]","EnumDevices method","IMDServiceProvider.EnumDevices","IMDServiceProvider::EnumDevices","IMDServiceProviderEnumDevices","mswmdm/IMDServiceProvider::EnumDevices","wmdm.imdserviceprovider_enumdevices"]
old-location: wmdm\imdserviceprovider_enumdevices.htm
tech.root: WMDM
ms.assetid: a3d4e404-7441-4a61-b2bb-ca373eb79b99
ms.date: 12/05/2018
ms.keywords: EnumDevices, EnumDevices method [windows Media Device Manager], EnumDevices method [windows Media Device Manager],IMDServiceProvider interface, IMDServiceProvider interface [windows Media Device Manager],EnumDevices method, IMDServiceProvider.EnumDevices, IMDServiceProvider::EnumDevices, IMDServiceProviderEnumDevices, mswmdm/IMDServiceProvider::EnumDevices, wmdm.imdserviceprovider_enumdevices
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
 - IMDServiceProvider::EnumDevices
 - mswmdm/IMDServiceProvider::EnumDevices
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
 - IMDServiceProvider.EnumDevices
---

# IMDServiceProvider::EnumDevices


## -description

The <b>EnumDevices</b> method enumerates the installed physical or software devices that are currently attached and are known by the service provider.

## -parameters

### -param ppEnumDevice [out]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice">IMDSPEnumDevice</a> interface. If the service provider implements <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice">IMDServiceProvider2::CreateDevice</a>, this enumerator should only enumerate non-Plug and Play devices.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is called on service providers that are not registered as Plug and Play aware (see <a href="/windows/desktop/WMDM/enabling-pnp-for-devices">Enabling PnP for Devices</a> and <a href="/windows/desktop/WMDM/enumerating-devices-service-provider">Enumerating Devices</a> for details). A service provider should return only the enumerator, which will enumerate only the devices that are currently attached to the computer and are supported by the service provider.

This method will be called only when an application starts, or when the application calls <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize">IWMDeviceManager2::Reinitialize</a>.

At present, Windows Media Device Manager does not support returning installed devices.

The service provider cannot alert the application when devices connect or disconnect from the computer. If a Plug and Play device connects or disconnects and an application implements <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification">IWMDMNotification</a>, then Windows Media Device Manager will send a notification to the application.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices-service-provider">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider">IMDServiceProvider Interface</a>