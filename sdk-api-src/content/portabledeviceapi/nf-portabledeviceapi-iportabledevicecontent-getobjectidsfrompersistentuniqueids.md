---
UID: NF:portabledeviceapi.IPortableDeviceContent.GetObjectIDsFromPersistentUniqueIDs
title: IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs
author: windows-driver-content
description: The GetObjectIDsFromPersistentUniqueIDs method retrieves the current object ID of one or more objects, given their persistent unique IDs (PUIDs).
old-location: wpdsdk\iportabledevicecontent_getobjectidsfrompersistentuniqueids.htm
old-project: wpd_sdk
ms.assetid: ee2aa718-0616-44b8-a9c6-cc835636500c
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetObjectIDsFromPersistentUniqueIDs, GetObjectIDsFromPersistentUniqueIDs method [Windows Portable Devices SDK], GetObjectIDsFromPersistentUniqueIDs method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],GetObjectIDsFromPersistentUniqueIDs method, IPortableDeviceContent.GetObjectIDsFromPersistentUniqueIDs, IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs, IPortableDeviceContentGetObjectIDsFromPersistentUniqueIDs, portabledeviceapi/IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs, wpdsdk.iportabledevicecontent_getobjectidsfrompersistentuniqueids
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceContent.GetObjectIDsFromPersistentUniqueIDs
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs


## -description



        The <b>GetObjectIDsFromPersistentUniqueIDs</b> method retrieves the current object ID of one or more objects, given their persistent unique IDs (PUIDs).
      


## -parameters




### -param pPersistentUniqueIDs [in]


            Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that contains one or more persistent unique ID (PUID) string values (type VT_LPWSTR).
          


### -param ppObjectIDs [out]


            Pointer to an <b>IPortableDevicePropVariantCollection</b> interface pointer that contains the retrieved object IDs, as type <b>VT_LPWSTR</b>. The retrieved IDs will be in the same order as the submitted PUIDs; if a value could not be found, it is indicated by an empty string. The caller must release this interface when it is done with it.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the required arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -remarks




        Windows Portable Devices Object IDs are unique across the device, but may be different across sessions. An Object ID can change when the application reconnects to the device.
      


        Certain applications, such as synchronization engines, require a way to identify the object across connection sessions. Every object has a WPD_OBJECT_PERSISTENT_UNIQUE_ID property, which indicates an identifier that is persistent across sessions. Applications can read and save this property in their initial session, by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a> method.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a03c673-8e7f-41a4-81ba-88406af2762d">IPortableDeviceContent Interface</a>



<a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>
 

 

