---
UID: NF:mswmdm.IMDServiceProvider.GetDeviceCount
title: IMDServiceProvider::GetDeviceCount
author: windows-sdk-content
description: The GetDeviceCount method returns the number of installed physical or software devices that are currently attached and are known by the service provider.
old-location: wmdm\imdserviceprovider_getdevicecount.htm
tech.root: WMDM
ms.assetid: 9cca4cb7-f569-452f-92dc-409b996ede17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDeviceCount, GetDeviceCount method [windows Media Device Manager], GetDeviceCount method [windows Media Device Manager],IMDServiceProvider interface, IMDServiceProvider interface [windows Media Device Manager],GetDeviceCount method, IMDServiceProvider.GetDeviceCount, IMDServiceProvider::GetDeviceCount, IMDServiceProviderGetDeviceCount, mswmdm/IMDServiceProvider::GetDeviceCount, wmdm.imdserviceprovider_getdevicecount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMDServiceProvider.GetDeviceCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The service provider should return only the number of supported devices that are currently attached to the computer.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider Interface</a>
 

 

