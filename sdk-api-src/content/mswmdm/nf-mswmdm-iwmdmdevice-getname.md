---
UID: NF:mswmdm.IWMDMDevice.GetName
title: IWMDMDevice::GetName
author: windows-sdk-content
description: The GetName method retrieves the human-readable name of the media device.
old-location: wmdm\iwmdmdevice_getname.htm
tech.root: WMDM
ms.assetid: 4bc5d550-6631-40ea-b020-2f5bb55899d6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetName, GetName method [windows Media Device Manager], GetName method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetName method, IWMDMDevice.GetName, IWMDMDevice::GetName, IWMDMDeviceGetName, mswmdm/IWMDMDevice::GetName, wmdm.iwmdmdevice_getname
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
 - IWMDMDevice.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IWMDMDevice.GetName
: 
---

# IWMDMDevice::GetName


## -description



The <b>GetName</b> method retrieves the human-readable name of the media device.




## -parameters




### -param pwszName [out]

Pointer to a (Unicode) wide-character, null-terminated string specifying the device name. The buffer is allocated and released by the caller.


### -param nMaxChars [in]

Integer specifying the maximum number of characters that can be placed in <i>pwszName</i>, including the termination character.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0">Exploring a Device</a>



<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>



<a href="https://msdn.microsoft.com/b240d6ac-99bd-4cc2-92d8-e9c7c5834bd7">IWMDMDevice::GetType</a>
 

 

