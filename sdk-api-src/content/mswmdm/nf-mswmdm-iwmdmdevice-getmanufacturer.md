---
UID: NF:mswmdm.IWMDMDevice.GetManufacturer
title: IWMDMDevice::GetManufacturer
author: windows-driver-content
description: The GetManufacturer method retrieves the name of the manufacturer of the device.
old-location: wmdm\iwmdmdevice_getmanufacturer.htm
old-project: WMDM
ms.assetid: 42e862e4-bfbc-4fca-b5df-001416173d6e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetManufacturer, GetManufacturer method [windows Media Device Manager], GetManufacturer method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetManufacturer method, IWMDMDevice.GetManufacturer, IWMDMDevice::GetManufacturer, IWMDMDeviceGetManufacturer, mswmdm/IWMDMDevice::GetManufacturer, wmdm.iwmdmdevice_getmanufacturer
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMDevice.GetManufacturer
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMDevice::GetManufacturer


## -description



The <b>GetManufacturer</b> method retrieves the name of the manufacturer of the device.




## -parameters




### -param pwszName [out]

Pointer to a wide-character, null-terminated string specifying the manufacturer's name. The buffer must be allocated and released by the caller.


### -param nMaxChars [in]

Integer specifying the maximum number of characters that can be copied to <i>pwszName</i>, including the termination character.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0">Exploring a Device</a>



<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>
 

 

