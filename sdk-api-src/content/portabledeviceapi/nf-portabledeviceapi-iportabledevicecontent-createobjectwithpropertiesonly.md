---
UID: NF:portabledeviceapi.IPortableDeviceContent.CreateObjectWithPropertiesOnly
title: IPortableDeviceContent::CreateObjectWithPropertiesOnly
author: windows-sdk-content
description: The CreateObjectWithPropertiesOnly method creates an object with only properties on the device.
old-location: wpdsdk\iportabledevicecontent_createobjectwithpropertiesonly.htm
old-project: wpd_sdk
ms.assetid: 0695d3d6-1f0d-45b4-8461-a76d759b6c09
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateObjectWithPropertiesOnly, CreateObjectWithPropertiesOnly method [Windows Portable Devices SDK], CreateObjectWithPropertiesOnly method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],CreateObjectWithPropertiesOnly method, IPortableDeviceContent.CreateObjectWithPropertiesOnly, IPortableDeviceContent::CreateObjectWithPropertiesOnly, IPortableDeviceContentCreateObjectWithPropertiesOnly, portabledeviceapi/IPortableDeviceContent::CreateObjectWithPropertiesOnly, wpdsdk.iportabledevicecontent_createobjectwithpropertiesonly
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceContent.CreateObjectWithPropertiesOnly
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceContent::CreateObjectWithPropertiesOnly


## -description


The <b>CreateObjectWithPropertiesOnly</b> method creates an object with only properties on the device.
      


## -parameters




### -param pValues

An IPortableDeviceValues collection of properties to assign to the object. For a list of required and optional properties for an object, see <a href="https://msdn.microsoft.com/4c3da994-fe12-4cb8-8f11-c4930cae96af">Requirements for Objects</a>.
          


### -param ppszObjectID [in, out]

An optional string pointer to receive the name of the new object. Can be <b>NULL</b>, if not needed. Windows Portable Devices defines the constant WPD_DEVICE_OBJECT_ID to represent a device. The SDK allocates this memory; the caller must release it using <b>CoTaskMemFree</b>.
          


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



Some objects are only a collection of properties—such as a folder, which is only a collection of pointers to other objects—while other objects are both properties and data—such as an audio file, which contains all the properties and the actual music bits. This method is used to create an object that contains only properties. To create an object with both properties and data, use <a href="https://msdn.microsoft.com/ea3445cc-69af-40a6-a5a4-695e0f2e1fb6">CreateObjectWithPropertiesAndData</a>.
      

This method is synchronous; when it returns, the new object should be present on the device.
      

The object that the driver actually creates might be a properties-and-data object, depending on what type of object is most convenient for the driver. To check what kind of object the driver has created, request the <a href="https://msdn.microsoft.com/en-us/library/Dd375704(v=VS.85).aspx">WPD_OBJECT_FORMAT</a> property of the new object.
      

The object will be created on the device when this method returns.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/6305cff9-c0ce-4ef5-a129-bc329b9c563f">Transferring a Properties-Only Object to the Device</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd388529(v=VS.85).aspx">IPortableDeviceContent Interface</a>



<a href="https://msdn.microsoft.com/6305cff9-c0ce-4ef5-a129-bc329b9c563f">Transferring a Properties-Only Object to the Device</a>
 

 

