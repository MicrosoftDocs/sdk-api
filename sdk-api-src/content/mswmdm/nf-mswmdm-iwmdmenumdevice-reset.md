---
UID: NF:mswmdm.IWMDMEnumDevice.Reset
title: IWMDMEnumDevice::Reset
author: windows-driver-content
description: The Reset method resets the enumeration so that Next returns a pointer to the first device.
old-location: wmdm\iwmdmenumdevice_reset.htm
old-project: WMDM
ms.assetid: af06bc07-2043-4ef5-a1f2-381797fb750b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWMDMEnumDevice interface [windows Media Device Manager],Reset method, IWMDMEnumDevice.Reset, IWMDMEnumDevice::Reset, IWMDMEnumDeviceReset, Reset, Reset method [windows Media Device Manager], Reset method [windows Media Device Manager],IWMDMEnumDevice interface, mswmdm/IWMDMEnumDevice::Reset, wmdm.iwmdmenumdevice_reset
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
-	IWMDMEnumDevice.Reset
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMEnumDevice::Reset


## -description



The <b>Reset</b> method resets the enumeration so that <a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a> returns a pointer to the first device.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice Interface</a>
 

 

