---
UID: NF:mswmdm.IMDSPDevice3.GetFormatCapability
title: IMDSPDevice3::GetFormatCapability method
author: windows-driver-content
description: The GetFormatCapability method retrieves information from a device about the values or ranges of values supported by the device for each aspect of a particular object format.
old-location: wmdm\imdspdevice3_getformatcapability.htm
old-project: WMDM
ms.assetid: ef53d7d2-dd9c-4705-9a25-9c0b16d03e7e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetFormatCapability method [windows Media Device Manager], GetFormatCapability method [windows Media Device Manager], IMDSPDevice3 interface, GetFormatCapability,IMDSPDevice3.GetFormatCapability, IMDSPDevice3, IMDSPDevice3 interface [windows Media Device Manager], GetFormatCapability method, IMDSPDevice3::GetFormatCapability, IMDSPDevice3GetFormatCapability, mswmdm/IMDSPDevice3::GetFormatCapability, wmdm.imdspdevice3_getformatcapability
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
-	IMDSPDevice3.GetFormatCapability
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMDSPDevice3::GetFormatCapability method


## -description



The <b>GetFormatCapability</b> method retrieves information from a device about the values or ranges of values supported by the device for each aspect of a particular object format.




## -parameters




### -param format [in]


<a href="https://msdn.microsoft.com/203d9bdf-cbbd-4d06-8292-26c8a472e2aa">WMDM_FORMATCODE</a>


Enumerated value representing inquired format.


### -param pFormatSupport [out]

Returned <a href="https://msdn.microsoft.com/9672173D-B11E-4DCB-BCAE-38B94FCC8B99">WMDM_FORMAT_CAPABILITY</a> structure containing the values or ranges of values supported for each aspect of a particular object format.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method can be called for any of the supported formats. The list of supported formats are represented by <b>g_wszWMDMFormatsSupported</b> device property.

For a particular format, this method should return all configurations of supported properties (for example, combinations of bit rate and sample rate). This information is expressed as a format capability. For detailed information, see <a href="https://msdn.microsoft.com/9672173D-B11E-4DCB-BCAE-38B94FCC8B99">WMDM_FORMAT_CAPABILITY</a>.




## -see-also




<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/e0665ba6-361d-488c-9100-68f39855b736">IMDSPDevice3::GetProperty</a>



<a href="https://msdn.microsoft.com/49d174b4-c8a3-4c16-ad21-4b66dcf8088f">WMDM_ENUM_PROP_VALID_VALUES_FORM</a>



<a href="https://msdn.microsoft.com/9672173D-B11E-4DCB-BCAE-38B94FCC8B99">WMDM_FORMAT_CAPABILITY</a>



<a href="https://msdn.microsoft.com/cf116861-e31d-4561-b262-e271888afc24">WMDM_PROP_CONFIG</a>



<a href="https://msdn.microsoft.com/e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2">WMDM_PROP_DESC</a>



<a href="https://msdn.microsoft.com/8094f3c0-a7ed-4e63-8503-aaac3fd9c012">WMDM_PROP_VALUES_ENUM</a>



<a href="https://msdn.microsoft.com/fb823a66-cc9c-4632-a4f0-03c7255c3ccb">WMDM_PROP_VALUES_RANGE</a>
 

 

