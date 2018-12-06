---
UID: NF:mswmdm.IMDSPStorage4.GetSpecifiedMetadata
title: IMDSPStorage4::GetSpecifiedMetadata
author: windows-sdk-content
description: The GetSpecifiedMetadata method retrieves only the specified metadata object for a storage.
old-location: wmdm\imdspstorage4_getspecifiedmetadata.htm
tech.root: WMDM
ms.assetid: 0f7b3a68-97b3-4470-8ca8-e8eb8a5f83b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSpecifiedMetadata, GetSpecifiedMetadata method [windows Media Device Manager], GetSpecifiedMetadata method [windows Media Device Manager],IMDSPStorage4 interface, IMDSPStorage4 interface [windows Media Device Manager],GetSpecifiedMetadata method, IMDSPStorage4.GetSpecifiedMetadata, IMDSPStorage4::GetSpecifiedMetadata, IMDSPStorage4GetSpecifiedMetadata, mswmdm/IMDSPStorage4::GetSpecifiedMetadata, wmdm.imdspstorage4_getspecifiedmetadata
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
 - IMDSPStorage4.GetSpecifiedMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorage4::GetSpecifiedMetadata


## -description



The <b>GetSpecifiedMetadata</b> method retrieves only the specified metadata object for a storage.




## -parameters




### -param cProperties [in]

Count of properties to be retrieved.


### -param ppwszPropNames [in]

Array that contains the property names to be retrieved. The size of this array should be equal to <i>cProperties</i>.


### -param pMetadata [out]

Pointer to the returned <b>IWMDMMetaData</b> interface pointer.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method gives the client control over which properties are retrieved. The client can specify the property names for the properties that the client needs to retrieve.

In contrast, the <b>GetMetadata</b> method retrieves all the storage metadata (properties).

If none of the specified properties can be returned, the service provider should return WMDM_E_NOTSUPPORTED or any suitable error code.

If at least one property can be retrieved, the service provider should return that property and set the return code to a success code of WMDM_S_NOT_ALL_PROPERTIES_RETRIEVED.




## -see-also




<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>
 

 

