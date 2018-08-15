---
UID: NF:mswmdm.IMDSPEnumDevice.Skip
title: IMDSPEnumDevice::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of media device interface(s) in the enumeration sequence.
old-location: wmdm\imdspenumdevice_skip.htm
old-project: WMDM
ms.assetid: 17b4e680-7f55-4f96-a0ca-acfda9f17784
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMDSPEnumDevice interface [windows Media Device Manager],Skip method, IMDSPEnumDevice.Skip, IMDSPEnumDevice::Skip, IMDSPEnumDeviceSkip, Skip, Skip method [windows Media Device Manager], Skip method [windows Media Device Manager],IMDSPEnumDevice interface, mswmdm/IMDSPEnumDevice::Skip, wmdm.imdspenumdevice_skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPEnumDevice.Skip
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPEnumDevice::Skip


## -description



The <b>Skip</b> method skips over the next specified number of media device interface(s) in the enumeration sequence.




## -parameters




### -param celt [in]

Number of elements to skip.


### -param pceltFetched [out]

Pointer to the number of elements that actually were skipped.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



If the number specified in the <i>celt</i> parameter is greater than the actual number of interfaces remaining in the enumeration sequence, then the return value from <b>Skip</b> is S_FALSE. When this happens, the <i>pceltFetched</i> parameter must be queried to determine how many interfaces were skipped. If you skip to the end of the array of enumerated media device interfaces, a subsequent call to <b>Next</b> returns S_FALSE.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/9a296937-6f8b-4f04-989f-3a5d4c6f7b85">IMDSPEnumDevice Interface</a>
 

 

