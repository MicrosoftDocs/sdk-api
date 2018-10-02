---
UID: NF:mswmdm.IMDSPEnumDevice.Next
title: IMDSPEnumDevice::Next
author: windows-sdk-content
description: The Next method retrieves a pointer to the next celtIMDSPDevice interfaces.
old-location: wmdm\imdspenumdevice_next.htm
tech.root: WMDM
ms.assetid: 137bcc3b-8c6e-4512-b564-a32af437f69a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMDSPEnumDevice interface [windows Media Device Manager],Next method, IMDSPEnumDevice.Next, IMDSPEnumDevice::Next, IMDSPEnumDeviceNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IMDSPEnumDevice interface, mswmdm/IMDSPEnumDevice::Next, wmdm.imdspenumdevice_next
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
 - IMDSPEnumDevice.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPEnumDevice::Next


## -description



The <b>Next</b> method retrieves a pointer to the next <i>celt</i><a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a> interfaces.




## -parameters




### -param celt [in]

Number of devices requested.


### -param ppDevice [out]

Array of <i>celt</i> pointers <a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a> allocated by the caller. Return <b>NULL</b> to indicate that no more devices exist or an error has occurred. If <i>celt</i> is more than 1, the caller must allocate enough memory to store <i>celt</i> number of interface pointers.


### -param pceltFetched [out]

Pointer to a <b>ULONG</b> variable that receives the number of interfaces retrieved.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



When there are no more service provider interfaces for enumerated devices, or when there are fewer of these interfaces than requested by the <i>celt</i> parameter, the return value from <b>Next</b> is S_FALSE. When this happens, the <i>pceltFetched</i> parameter must be queried to determine how many interfaces, if any, were returned.

The device enumerator may not reflect the effect of device insertion and removal.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>



<a href="https://msdn.microsoft.com/9a296937-6f8b-4f04-989f-3a5d4c6f7b85">IMDSPEnumDevice Interface</a>
 

 

