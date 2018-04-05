---
UID: NF:mswmdm.IMDSPDevice2.GetSpecifyPropertyPages
title: IMDSPDevice2::GetSpecifyPropertyPages method
author: windows-driver-content
description: The GetSpecifyPropertyPages method gets property pages describing non-standard capabilities of portable devices.
old-location: wmdm\imdspdevice2_getspecifypropertypages.htm
old-project: WMDM
ms.assetid: e79ce0d2-bfea-4a5b-82f8-9d69f96d9698
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetSpecifyPropertyPages method [windows Media Device Manager], GetSpecifyPropertyPages method [windows Media Device Manager], IMDSPDevice2 interface, GetSpecifyPropertyPages,IMDSPDevice2.GetSpecifyPropertyPages, IMDSPDevice2, IMDSPDevice2 interface [windows Media Device Manager], GetSpecifyPropertyPages method, IMDSPDevice2::GetSpecifyPropertyPages, IMDSPDevice2GetSpecifyPropertyPages, mswmdm/IMDSPDevice2::GetSpecifyPropertyPages, wmdm.imdspdevice2_getspecifypropertypages
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
-	IMDSPDevice2.GetSpecifyPropertyPages
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMDSPDevice2::GetSpecifyPropertyPages method


## -description



The <b>GetSpecifyPropertyPages</b> method gets property pages describing non-standard capabilities of portable devices.




## -parameters




### -param ppSpecifyPropPages [out]

Pointer to a Win32 <b>ISpecifyPropertyPages</b> interface pointer.


### -param pppUnknowns [out]

Array of <b>IUnknown</b> interface pointers. These interfaces will be passed to the property page and can be used to pass information between the property page and the service provider.


### -param pcUnks [out]

Size of the <i>pppUnknowns</i> array.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Memory for the <i>pppUnknowns</i> array should be allocated by this method and must be freed by the caller using <b>CoTaskMemFree</b>, a standard Win32 function.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2 Interface</a>
 

 

