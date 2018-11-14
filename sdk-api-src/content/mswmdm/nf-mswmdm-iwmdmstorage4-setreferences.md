---
UID: NF:mswmdm.IWMDMStorage4.SetReferences
title: IWMDMStorage4::SetReferences
author: windows-sdk-content
description: The SetReferences method sets the references contained in a storage that has references (such as a playlist or album), overwriting any previously existing references held by the storage.
old-location: wmdm\iwmdmstorage4_setreferences.htm
tech.root: WMDM
ms.assetid: f61b8c4e-6ea1-49a3-8b61-c3ea8bfe2714
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWMDMStorage4 interface [windows Media Device Manager],SetReferences method, IWMDMStorage4.SetReferences, IWMDMStorage4::SetReferences, IWMDMStorage4SetReferences, SetReferences, SetReferences method [windows Media Device Manager], SetReferences method [windows Media Device Manager],IWMDMStorage4 interface, mswmdm/IWMDMStorage4::SetReferences, wmdm.iwmdmstorage4_setreferences
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
 - IWMDMStorage4.SetReferences
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IWMDMStorage4.SetReferences
: 
---

# IWMDMStorage4::SetReferences


## -description



The <b>SetReferences</b> method sets the references contained in a storage that has references (such as a playlist or album), overwriting any previously existing references held by the storage.




## -parameters




### -param dwRefs [in]

Count of <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface pointers in <i>ppIWMDMStorage</i>. Zero is an acceptable value and clears all references from the storage. The storage itself is not deleted in this case.


### -param ppIWMDMStorage [in]

Pointer to an array of <b>IWMDMStorage</b> interface pointers to be referenced by the storage. This order is preserved by the storage. <b>NULL</b> is an acceptable value if <i>dwRefs</i> is also zero. The caller is responsible for allocating and releasing this array.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method is used to set references in objects that are composed of references, such as playlists or albums. If a device does not support metadata, this method will probably not be supported.

Any valid <b>IWMDMStorage</b> object can be contained in the <i>ppIWMDMStorage</i> array. This includes folders and other storages specifying references themselves (creating, for example, a playlist of playlists). The device itself determines how any particular case of referent object is handled. Windows Media Device Manager does not enforce any rules beyond that of <b>IWMDMStorage</b> validity. Consider the case of a playlist containing nested playlist references. On one device, this is disallowed and <b>SetReferences</b> fails. On another device, this is allowed; playback simply traverses the entire set of contained references in depth-first order.

The situation may arise where an <b>IWMDMStorage4</b> interface pointer corresponds to a storage that no longer exists on the device. WMDM_E_INTERFACEDEAD is returned in this case.




## -see-also




<a href="https://msdn.microsoft.com/9f803e1a-ff33-443a-9448-e8c875d77e51">Creating a Playlist on the Device</a>



<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>



<a href="https://msdn.microsoft.com/8199de99-3660-4819-a8e0-ae8e3aa1680e">IWMDMStorage4::GetReferences</a>
 

 

