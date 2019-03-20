---
UID: NF:mswmdm.IWMDeviceManager.EnumDevices
title: IWMDeviceManager::EnumDevices (mswmdm.h)
author: windows-sdk-content
description: The EnumDevices method retrieves a pointer to the IWMDMEnumDevice interface that can be used to enumerate portable devices connected to the computer.
old-location: wmdm\iwmdevicemanager_enumdevices.htm
tech.root: WMDM
ms.assetid: 1daa6d36-9858-4504-a9a2-c0341031829b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumDevices, EnumDevices method [windows Media Device Manager], EnumDevices method [windows Media Device Manager],IWMDeviceManager interface, IWMDeviceManager interface [windows Media Device Manager],EnumDevices method, IWMDeviceManager.EnumDevices, IWMDeviceManager::EnumDevices, IWMDeviceManagerEnumDevices, mswmdm/IWMDeviceManager::EnumDevices, wmdm.iwmdevicemanager_enumdevices
ms.topic: method
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
 - IWMDeviceManager.EnumDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDeviceManager::EnumDevices


## -description



The <b>EnumDevices</b> method retrieves a pointer to the <a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice</a> interface that can be used to enumerate portable devices connected to the computer.




## -parameters




### -param ppEnumDevice [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice</a> interface used to enumerate devices. The caller must release this interface when done with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method returns devices based on earlier versions of Windows Media Device Manager. To get all devices, including newer devices (such as MTP devices), call <a href="https://msdn.microsoft.com/b5015263-23f2-466f-a89f-26c14f7a2263">IWMDMDeviceManager2::EnumDevices2</a>.




## -see-also




<a href="https://msdn.microsoft.com/c5935681-b530-4446-a026-7ddc74084d23">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice Interface</a>



<a href="https://msdn.microsoft.com/cac68821-42fc-4833-bf2e-eec1768869e6">IWMDeviceManager Interface</a>



<a href="https://msdn.microsoft.com/b5015263-23f2-466f-a89f-26c14f7a2263">IWMDeviceManager2::EnumDevices2</a>
 

 

