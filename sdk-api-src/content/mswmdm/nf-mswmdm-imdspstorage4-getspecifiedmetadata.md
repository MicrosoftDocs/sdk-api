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

# IMDSPStorage4::GetSpecifiedMetadata


## -description



The <b>GetSpecifiedMetadata</b> method retrieves only the specified metadata object for a storage.




## -parameters




### -param cProperties [in]

Count of properties to be retrieved.


### -param ppwszPropNames [in]

Array that contains the property names to be retrieved. The size of this array should be equal to <i>cProperties</i>.


### -param pMetadata






#### - ppMetadata [out]

Pointer to the returned <b>IWMDMMetaData</b> interface pointer.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method gives the client control over which properties are retrieved. The client can specify the property names for the properties that the client needs to retrieve.

In contrast, the <b>GetMetadata</b> method retrieves all the storage metadata (properties).

If none of the specified properties can be returned, the service provider should return WMDM_E_NOTSUPPORTED or any suitable error code.

If at least one property can be retrieved, the service provider should return that property and set the return code to a success code of WMDM_S_NOT_ALL_PROPERTIES_RETRIEVED.




## -see-also




<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>
 

 

