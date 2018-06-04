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

# IMDSPStorage4::SetReferences


## -description



The <b>SetReferences</b> method sets the references contained in a storage that has references (such as playlist/album), overwriting any previously existing references contained in this storage.




## -parameters




### -param dwRefs [in]

Count of <b>IMDSPStorage</b> interface pointers contained in the passed-in array. Zero is an acceptable value and resets the storage to contain zero references. The storage itself is not deleted in this case.


### -param ppISPStorage






#### - ppIWMDMStorage [in]

Pointer to an array of <b>IMDSPStorage</b> interface pointers used to set references in a storage. The ordering of references matches the ordering of the corresponding <b>IWMDMStorage</b> interface pointers in this array. <b>NULL</b> is an acceptable value if <i>dwRefs</i> is also zero.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Any valid <b>IMDSPStorage</b> object may be contained in the <i>ppIMDSPStorage</i> array. This includes folders and other storages containing references themselves (creating, for example, a playlist of playlists).

Depending upon the level of support in the device (whether it supports playlists or nested playlists), the service provider should handle this method appropriately. If the device does not have the level of supported needed for the passed-in reference array, the service provider should return WMDM_E_NOTSUPPORTED.

If the reference contains a deleted storage, WMDM_E_INTERFACEDEAD should be returned.

The <b>SetReferences</b> method follows a wipe-and-load model. The references passed include a complete set and should replace any existing references on the storage object completely.




## -see-also




<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>



<a href="https://msdn.microsoft.com/f8caf10b-69d4-4d37-836e-af260840254f">IMDSPStorage4::GetReferences</a>
 

 

