---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetFunctionalObjects
title: IPortableDeviceCapabilities::GetFunctionalObjects method
author: windows-driver-content
description: The GetFunctionalObjects method retrieves all functional objects that match a specified category on the device.
old-location: wpdsdk\iportabledevicecapabilities_getfunctionalobjects.htm
old-project: wpd_sdk
ms.assetid: 46657e4d-c2fe-42bf-9a3d-5075d4f3ee91
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetFunctionalObjects method [Windows Portable Devices SDK], GetFunctionalObjects method [Windows Portable Devices SDK], IPortableDeviceCapabilities interface, GetFunctionalObjects,IPortableDeviceCapabilities.GetFunctionalObjects, IPortableDeviceCapabilities, IPortableDeviceCapabilities interface [Windows Portable Devices SDK], GetFunctionalObjects method, IPortableDeviceCapabilities::GetFunctionalObjects, IPortableDeviceCapabilitiesGetFunctionalObjects, portabledeviceapi/IPortableDeviceCapabilities::GetFunctionalObjects, wpdsdk.iportabledevicecapabilities_getfunctionalobjects
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
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceCapabilities.GetFunctionalObjects
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceCapabilities::GetFunctionalObjects method


## -description



        The <a href="https://msdn.microsoft.com/c292a509-f202-4136-bbf7-b4e82ef2b936">GetFunctionalObjects</a> method retrieves all functional objects that match a specified category on the device.
      


## -parameters




### -param Category [in]


            A <b>REFGUID</b> that specifies the category to search for. This can be WPD_FUNCTIONAL_CATEGORY_ALL to return all functional objects.
          


### -param ppObjectIDs [out]


            Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that contains the object IDs of the functional objects as strings (type VT_LPWSTR in the retrieved <b>PROPVARIANT</b> items). If no objects of the requested type are found, this will be an empty collection (not <b>NULL</b>). The caller must release this interface when it is done with it.
          


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
</table>
 




## -remarks




        This operation is usually fast, because the driver does not need to perform a full content enumeration, and the number of retrieved functional objects is typically less than 10. If no objects of the requested type are found, this method will not return an error, but returns an empty collection for <i>ppObjectIDs</i>.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/9a13071a-95a1-4330-92d5-11fa72a8f211">Retrieving the Functional Object Identifiers for a Device</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c292a509-f202-4136-bbf7-b4e82ef2b936">IPortableDeviceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/9a13071a-95a1-4330-92d5-11fa72a8f211">Retrieving the Functional Object Identifiers for a Device</a>



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>
 

 

