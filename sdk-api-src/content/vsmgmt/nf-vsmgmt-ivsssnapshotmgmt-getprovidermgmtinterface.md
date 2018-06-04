---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IVssSnapshotMgmt::GetProviderMgmtInterface


## -description


The 
    <b>GetProviderMgmtInterface</b> 
    method returns an interface to further configure the system provider.


## -parameters




### -param ProviderId [in]

This must be the system provider. The  <b>VSS_ID</b> for the system provider <code>{b5946137-7b9f-4925-af80-51abd60b20d5}</code>.


### -param InterfaceId [in]

Must be <b>IID_IVssDifferentialSoftwareSnapshotMgmt</b>, which represents the 
      <a href="https://msdn.microsoft.com/d322981f-1916-4d38-9d05-bc3db2cd596d">IVssDifferentialSoftwareSnapshotMgmt</a> 
      interface.


### -param ppItf [out]

Address of an interface pointer that is filled in with the returned interface pointer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d322981f-1916-4d38-9d05-bc3db2cd596d">IVssDifferentialSoftwareSnapshotMgmt</a>



<a href="https://msdn.microsoft.com/5e5694a1-7c17-4d8a-b094-09dcf28a636f">IVssSnapshotMgmt</a>
 

 

