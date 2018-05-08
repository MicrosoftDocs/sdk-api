---
UID: NF:portabledeviceapi.IPortableDeviceResources.GetResourceAttributes
title: IPortableDeviceResources::GetResourceAttributes
author: windows-driver-content
description: The GetResourceAttributes method retrieves all attributes from a specified resource in an object.
old-location: wpdsdk\iportabledeviceresources_getresourceattributes.htm
old-project: wpd_sdk
ms.assetid: 6188d0cc-3161-400e-9abf-ef43a4dee690
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetResourceAttributes, GetResourceAttributes method [Windows Portable Devices SDK], GetResourceAttributes method [Windows Portable Devices SDK],IPortableDeviceResources interface, IPortableDeviceResources interface [Windows Portable Devices SDK],GetResourceAttributes method, IPortableDeviceResources.GetResourceAttributes, IPortableDeviceResources::GetResourceAttributes, IPortableDeviceResourcesGetResourceAttributes, portabledeviceapi/IPortableDeviceResources::GetResourceAttributes, wpdsdk.iportabledeviceresources_getresourceattributes
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
-	IPortableDeviceResources.GetResourceAttributes
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDeviceResources::GetResourceAttributes


## -description



The <b>GetResourceAttributes</b> method retrieves all attributes from a specified resource in an object.




## -parameters




### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object hosting the resource.


### -param Key [in]

A <b>REFPROPERTYKEY</b> that specifies which resource to query.


### -param ppResourceAttributes [out]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface pointer that holds <b>PROPERTYKEY</b>/<b>PROPVARIANT</b> pairs that describe each attribute and its value, respectively. The value types of the attribute values vary. If a property could not be returned, the value for the returned property will be <b>VT_ERROR</b>, and the <b>PROPVARIANT</b> <i>scode</i> member will contain the <b>HRESULT</b> of that particular failure.


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
All attribute values were retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
One or more attribute values could not be retrieved. These will have <b>HRESULT</b> values of type VT_ERROR in the retrieved <i>ppResourceAttributes</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the required pointer arguments was <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Resource attributes describe the access rights, size, format, and other information related to a resource. For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.




## -see-also




<a href="https://msdn.microsoft.com/fce2d6db-13f0-4c1d-ba55-16139c6acbb7">IPortableDeviceResources Interface</a>
 

 

