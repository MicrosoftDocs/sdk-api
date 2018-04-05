---
UID: NF:portabledeviceapi.IPortableDeviceProperties.SetValues
title: IPortableDeviceProperties::SetValues method
author: windows-driver-content
description: The SetValues method adds or modifies one or more properties on a specified object on a device.
old-location: wpdsdk\iportabledeviceproperties_setvalues.htm
old-project: wpd_sdk
ms.assetid: 3c631d31-5553-4ad0-8384-821c11c78254
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceProperties, IPortableDeviceProperties interface [Windows Portable Devices SDK], SetValues method, IPortableDeviceProperties::SetValues, IPortableDevicePropertiesSetValues, SetValues method [Windows Portable Devices SDK], SetValues method [Windows Portable Devices SDK], IPortableDeviceProperties interface, SetValues,IPortableDeviceProperties.SetValues, portabledeviceapi/IPortableDeviceProperties::SetValues, wpdsdk.iportabledeviceproperties_setvalues
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
-	IPortableDeviceProperties.SetValues
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceProperties::SetValues method


## -description



The <b>SetValues</b> method adds or modifies one or more properties on a specified object on a device.




## -parameters




### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object to modify. To specify the device, use WPD_DEVICE_OBJECT_ID.


### -param pValues [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains one or more property/value pairs to set. Existing values will be overwritten.


### -param ppResults [out]

Address of a variable that receives a pointer to an <b>IPortableDeviceValues</b> interface that contains a collection of property/HRESULT values. Each value (type VT_ERROR) describes the success or failure of the property set attempt. The caller must release this interface when it is done with it.


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
All specified property values were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
One or more properties could not be modified. Those that could not will have an <b>HRESULT</b> of type VT_ERROR in the retrieved <i>ppResults</i> parameter.

</td>
</tr>
</table>
 




## -remarks



To delete a property, call <a href="https://msdn.microsoft.com/2547c9aa-edc7-4331-b5f2-bfb4a96f7175">IPortableDeviceProperties::Delete</a>. A property can be deleted only if its WPD_PROPERTY_ATTRIBUTE_CAN_WRITE attribute is True. This attribute can be retrieved by calling <a href="https://msdn.microsoft.com/bb2206ff-e1d4-4bc5-819b-b008a293c43d">GetPropertyAttributes</a>.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/1c003534-96b4-419b-94d1-73b5ffa2eba1">Setting Properties for a Single Object</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4555e85b-c667-466c-a527-cc29ca7a6aee">IPortableDeviceProperties Interface</a>



<a href="https://msdn.microsoft.com/2547c9aa-edc7-4331-b5f2-bfb4a96f7175">IPortableDeviceProperties::Delete</a>



<a href="https://msdn.microsoft.com/5f4ec65c-dd26-40d5-a9f8-a2175c3aa54c">IPortableDeviceProperties::GetValues</a>



<a href="https://msdn.microsoft.com/1c003534-96b4-419b-94d1-73b5ffa2eba1">Setting Properties for a Single Object</a>



<a href="https://msdn.microsoft.com/f762a571-83ea-4999-ad49-a51044bc790d">Writing Content-Object Properties</a>
 

 

