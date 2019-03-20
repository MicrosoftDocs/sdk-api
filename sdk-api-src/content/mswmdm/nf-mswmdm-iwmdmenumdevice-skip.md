---
UID: NF:mswmdm.IWMDMEnumDevice.Skip
title: IWMDMEnumDevice::Skip (mswmdm.h)
author: windows-sdk-content
description: The Skip method skips over a specified number of devices in the enumeration sequence.
old-location: wmdm\iwmdmenumdevice_skip.htm
tech.root: WMDM
ms.assetid: fd6d2066-5445-4e29-812f-7d52dc67d57a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMDMEnumDevice interface [windows Media Device Manager],Skip method, IWMDMEnumDevice.Skip, IWMDMEnumDevice::Skip, IWMDMEnumDeviceSkip, Skip, Skip method [windows Media Device Manager], Skip method [windows Media Device Manager],IWMDMEnumDevice interface, mswmdm/IWMDMEnumDevice::Skip, wmdm.iwmdmenumdevice_skip
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
 - IWMDMEnumDevice.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMEnumDevice::Skip


## -description



The <b>Skip</b> method skips over a specified number of devices in the enumeration sequence.




## -parameters




### -param celt [in]

Number of devices to skip.


### -param pceltFetched [out]

Number of devices actually skipped.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



If the requested number of devices to skip is greater than the remaining devices, the return value from <b>Skip</b> is S_FALSE. At this point, <i>pceltFetched</i> must be used to determine the number of interfaces skipped. If you skip to the end of the device array, a subsequent call to <i>Next</i> also returns S_FALSE. For more information about the standard enumerator Skip method, see the Microsoft COM documentation, available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=3282">Microsoft Web site</a>.




## -see-also




<a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice Interface</a>
 

 

