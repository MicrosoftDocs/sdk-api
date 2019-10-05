---
UID: NF:mswmdm.IWMDMDevice.EnumStorage
title: IWMDMDevice::EnumStorage (mswmdm.h)
author: windows-sdk-content
description: The EnumStorage method retrieves an IWMDMEnumStorage interface to enumerate the storages on a device.
old-location: wmdm\iwmdmdevice_enumstorage.htm
tech.root: WMDM
ms.assetid: ffd3c51a-7ec2-4ce5-9260-2b08bfa88a99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumStorage, EnumStorage method [windows Media Device Manager], EnumStorage method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],EnumStorage method, IWMDMDevice.EnumStorage, IWMDMDevice::EnumStorage, IWMDMDeviceEnumStorage, mswmdm/IWMDMDevice::EnumStorage, wmdm.iwmdmdevice_enumstorage
ms.topic: method
f1_keywords: 
 - "mswmdm/IWMDMDevice.EnumStorage"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDevice.EnumStorage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMDevice::EnumStorage


## -description



The <b>EnumStorage</b> method retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage</a> interface to enumerate the storages on a device.



Syntax


## -parameters




### -param ppEnumStorage [out]

Pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage</a> interface to enumerate the storages on a device. This points to the root storage on the device. The caller is responsible for calling <b>Release</b> on the retrieved interface.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/error-codes">Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage Interface</a>
 

 

