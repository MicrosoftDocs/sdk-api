---
UID: NF:mswmdm.IMDSPStorageGlobals.GetDevice
title: IMDSPStorageGlobals::GetDevice method
author: windows-driver-content
description: The GetDevice method retrieves a pointer to the device on which the storage medium with which this interface is associated is mounted.
old-location: wmdm\imdspstorageglobals_getdevice.htm
old-project: WMDM
ms.assetid: 5c35b426-f7fd-46f7-b92d-12a0c22b50e9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetDevice method [windows Media Device Manager], GetDevice method [windows Media Device Manager], IMDSPStorageGlobals interface, GetDevice,IMDSPStorageGlobals.GetDevice, IMDSPStorageGlobals, IMDSPStorageGlobals interface [windows Media Device Manager], GetDevice method, IMDSPStorageGlobals::GetDevice, IMDSPStorageGlobalsGetDevice, mswmdm/IMDSPStorageGlobals::GetDevice, wmdm.imdspstorageglobals_getdevice
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
-	IMDSPStorageGlobals.GetDevice
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMDSPStorageGlobals::GetDevice method


## -description



The <b>GetDevice</b> method retrieves a pointer to the device on which the storage medium with which this interface is associated is mounted.




## -parameters




### -param ppDevice [out]

Pointer to a device identified by the <b>IMDSPDevice</b> interface.


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




<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>
 

 

