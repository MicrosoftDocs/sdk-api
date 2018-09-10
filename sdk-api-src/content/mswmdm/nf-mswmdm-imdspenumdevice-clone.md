---
UID: NF:mswmdm.IMDSPEnumDevice.Clone
title: IMDSPEnumDevice::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: wmdm\imdspenumdevice_clone.htm
tech.root: WMDM
ms.assetid: fe6b8766-4f63-4a6c-b7dd-39a304679185
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Clone, Clone method [windows Media Device Manager], Clone method [windows Media Device Manager],IMDSPEnumDevice interface, IMDSPEnumDevice interface [windows Media Device Manager],Clone method, IMDSPEnumDevice.Clone, IMDSPEnumDevice::Clone, IMDSPEnumDeviceClone, mswmdm/IMDSPEnumDevice::Clone, wmdm.imdspenumdevice_clone
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
 - IMDSPEnumDevice.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPEnumDevice::Clone


## -description



The <b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.




## -parameters




### -param ppEnumDevice [out]

Pointer to an <a href="https://msdn.microsoft.com/9a296937-6f8b-4f04-989f-3a5d4c6f7b85">IMDSPEnumDevice</a> interface.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



Using this function, a client can record a particular point in the enumeration sequence, and then return to that point later. The new enumerator supports the same interface as the original one.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/9a296937-6f8b-4f04-989f-3a5d4c6f7b85">IMDSPEnumDevice Interface</a>
 

 

