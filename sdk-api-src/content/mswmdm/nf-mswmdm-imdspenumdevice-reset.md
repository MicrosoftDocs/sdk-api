---
UID: NF:mswmdm.IMDSPEnumDevice.Reset
title: IMDSPEnumDevice::Reset (mswmdm.h)
author: windows-sdk-content
description: The Reset method resets the enumeration sequence to the beginning. A subsequent call to Next fetches the first Windows Media Device Manager interface in the enumeration sequence.
old-location: wmdm\imdspenumdevice_reset.htm
tech.root: WMDM
ms.assetid: 7edd0d45-aeae-4bc8-b4d4-f74bcb403ef9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPEnumDevice interface [windows Media Device Manager],Reset method, IMDSPEnumDevice.Reset, IMDSPEnumDevice::Reset, IMDSPEnumDeviceReset, Reset, Reset method [windows Media Device Manager], Reset method [windows Media Device Manager],IMDSPEnumDevice interface, mswmdm/IMDSPEnumDevice::Reset, wmdm.imdspenumdevice_reset
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
 - IMDSPEnumDevice.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPEnumDevice::Reset


## -description



The <b>Reset</b> method resets the enumeration sequence to the beginning. A subsequent call to <b>Next</b> fetches the first Windows Media Device Manager interface in the enumeration sequence.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/9a296937-6f8b-4f04-989f-3a5d4c6f7b85">IMDSPEnumDevice Interface</a>
 

 

