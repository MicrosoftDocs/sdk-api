---
UID: NF:mswmdm.IMDServiceProvider.EnumDevices
title: IMDServiceProvider::EnumDevices (mswmdm.h)
author: windows-sdk-content
description: The EnumDevices method enumerates the installed physical or software devices that are currently attached and are known by the service provider.
old-location: wmdm\imdserviceprovider_enumdevices.htm
tech.root: WMDM
ms.assetid: a3d4e404-7441-4a61-b2bb-ca373eb79b99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumDevices, EnumDevices method [windows Media Device Manager], EnumDevices method [windows Media Device Manager],IMDServiceProvider interface, IMDServiceProvider interface [windows Media Device Manager],EnumDevices method, IMDServiceProvider.EnumDevices, IMDServiceProvider::EnumDevices, IMDServiceProviderEnumDevices, mswmdm/IMDServiceProvider::EnumDevices, wmdm.imdserviceprovider_enumdevices
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
 - IMDServiceProvider.EnumDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDServiceProvider::EnumDevices


## -description



The <b>EnumDevices</b> method enumerates the installed physical or software devices that are currently attached and are known by the service provider.




## -parameters




### -param ppEnumDevice [out]

Pointer to an <a href="https://msdn.microsoft.com/9a296937-6f8b-4f04-989f-3a5d4c6f7b85">IMDSPEnumDevice</a> interface. If the service provider implements <a href="https://msdn.microsoft.com/f724ef14-c572-41ca-a56b-fde85d7620e0">IMDServiceProvider2::CreateDevice</a>, this enumerator should only enumerate non-Plug and Play devices.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method is called on service providers that are not registered as Plug and Play aware (see <a href="https://msdn.microsoft.com/510237a9-2b74-4c2e-ad45-3f45117289a6">Enabling PnP for Devices</a> and <a href="https://msdn.microsoft.com/7602da65-4c98-4766-b206-2129dad4cc2a">Enumerating Devices</a> for details). A service provider should return only the enumerator, which will enumerate only the devices that are currently attached to the computer and are supported by the service provider.

This method will be called only when an application starts, or when the application calls <a href="https://msdn.microsoft.com/9eabf5ff-96e1-426f-ae31-197a2165a743">IWMDeviceManager2::Reinitialize</a>.

At present, Windows Media Device Manager does not support returning installed devices.

The service provider cannot alert the application when devices connect or disconnect from the computer. If a Plug and Play device connects or disconnects and an application implements <a href="https://msdn.microsoft.com/3089a04d-24f5-4a4c-9df5-b4073fef358a">IWMDMNotification</a>, then Windows Media Device Manager will send a notification to the application.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/7602da65-4c98-4766-b206-2129dad4cc2a">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider Interface</a>
 

 

