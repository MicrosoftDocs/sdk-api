---
UID: NF:mswmdm.IMDSPDevice.EnumStorage
title: IMDSPDevice::EnumStorage
author: windows-sdk-content
description: The EnumStorage method retrieves a pointer to an IMDSPEnumStorage interface of an enumerator object that represents the top-level storage(s) on the device. Top-level storage for a device is the root directory of the storage medium.
old-location: wmdm\imdspdevice_enumstorage.htm
old-project: WMDM
ms.assetid: bbf19979-8e09-476e-9401-443ab5e84866
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: EnumStorage, EnumStorage method [windows Media Device Manager], EnumStorage method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],EnumStorage method, IMDSPDevice.EnumStorage, IMDSPDevice::EnumStorage, IMDSPDeviceEnumStorage, mswmdm/IMDSPDevice::EnumStorage, wmdm.imdspdevice_enumstorage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IMDSPDevice.EnumStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice::EnumStorage


## -description



The <b>EnumStorage</b> method retrieves a pointer to an <b>IMDSPEnumStorage</b> interface of an enumerator object that represents the top-level storage(s) on the device. Top-level storage for a device is the root directory of the storage medium.




## -parameters




### -param ppEnumStorage [out]

Pointer to an <a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage</a> object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>
 

 

