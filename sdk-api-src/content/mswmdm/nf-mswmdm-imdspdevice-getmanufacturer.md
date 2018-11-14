---
UID: NF:mswmdm.IMDSPDevice.GetManufacturer
title: IMDSPDevice::GetManufacturer
author: windows-sdk-content
description: The GetManufacturer method retrieves the name of the manufacturer of the device.
old-location: wmdm\imdspdevice_getmanufacturer.htm
tech.root: WMDM
ms.assetid: 5dc5abe8-f43b-4cff-baa1-cef9e2c1a7a4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetManufacturer, GetManufacturer method [windows Media Device Manager], GetManufacturer method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetManufacturer method, IMDSPDevice.GetManufacturer, IMDSPDevice::GetManufacturer, IMDSPDeviceGetManufacturer, mswmdm/IMDSPDevice::GetManufacturer, wmdm.imdspdevice_getmanufacturer
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
 - IMDSPDevice.GetManufacturer
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
- IMDSPDevice.GetManufacturer
: 
---

# IMDSPDevice::GetManufacturer


## -description



The <b>GetManufacturer</b> method retrieves the name of the manufacturer of the device.




## -parameters




### -param pwszName [out]

Pointer to a caller-allocated wide character array that receives the manufacturer name string.


### -param nMaxChars [in]

Maximum number of characters to copy to the string, including the termination character.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The <b>LPWSTR</b> string type is a 16-bit Unicode character string and does not accept byte-sized characters. To convert a string of byte-sized characters (<b>LPCSTR</b>) to an <b>LPWSTR</b> string, use the <b>MultiByteToWideChar</b> function, as described in the Microsoft® Windows® Platform Software Development Kit documentation.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>
 

 

