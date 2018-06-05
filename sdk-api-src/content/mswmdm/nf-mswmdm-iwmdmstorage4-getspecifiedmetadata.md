---
UID: NF:mswmdm.IWMDMStorage4.GetSpecifiedMetadata
title: IWMDMStorage4::GetSpecifiedMetadata
author: windows-sdk-content
description: The GetSpecifiedMetadata method retrieves one or more specific metadata properties from the storage.
old-location: wmdm\iwmdmstorage4_getspecifiedmetadata.htm
old-project: WMDM
ms.assetid: c4e2c889-9ad0-42d1-bb50-4ebcb9859715
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetSpecifiedMetadata, GetSpecifiedMetadata method [windows Media Device Manager], GetSpecifiedMetadata method [windows Media Device Manager],IWMDMStorage4 interface, IWMDMStorage4 interface [windows Media Device Manager],GetSpecifiedMetadata method, IWMDMStorage4.GetSpecifiedMetadata, IWMDMStorage4::GetSpecifiedMetadata, IWMDMStorage4GetSpecifiedMetadata, mswmdm/IWMDMStorage4::GetSpecifiedMetadata, wmdm.iwmdmstorage4_getspecifiedmetadata
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
-	IWMDMStorage4.GetSpecifiedMetadata
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage4::GetSpecifiedMetadata


## -description



The <b>GetSpecifiedMetadata</b> method retrieves one or more specific metadata properties from the storage.




## -parameters




### -param cProperties [in]

Count of properties to retrieve.


### -param ppwszPropNames [in]

Array of property names to retrieve. The length of this array should be equal to <i>cProperties</i>. The application should free this memory using <b>CoTaskMemFree</b>.


### -param ppMetadata [out]

Pointer to the returned <a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData</a> interface pointer, containing the retrieved values. The caller must release this interface when finished with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method gives the client control over which properties are retrieved. This can be more efficient than <a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a>, and is recommended when the client needs only a subset of properties supported by the storage.

If this method is used to retrieve data from a Windows Portable Devices (WPD) device, the data is returned in binary form in an <b>IPortableDeviceValues</b> object. The application should de-serialize this data in order to obtain the actual property values.

The method succeeds and returns WMDM_S_NOT_ALL_PROPERTIES_RETRIEVED even if some of the specified properties could not be retrieved (but at least one property was retrieved). The method fails and returns WMDM_E_NOTSUPPORTED if none of the specified properties could be retrieved.

Requesting a single property is a special case of this method. If the client requests a single property, the possible return codes are S_OK, E_INVALIDARG, and WMDM_E_NOTSUPPORTED. Thus, in the case of a single property, the method succeeds only if the property is successfully retrieved.




## -see-also




<a href="https://msdn.microsoft.com/9f803e1a-ff33-443a-9448-e8c875d77e51">Creating a Playlist on the Device</a>



<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>
 

 

