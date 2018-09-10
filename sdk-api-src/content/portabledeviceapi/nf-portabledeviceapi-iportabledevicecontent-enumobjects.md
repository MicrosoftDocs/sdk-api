---
UID: NF:portabledeviceapi.IPortableDeviceContent.EnumObjects
title: IPortableDeviceContent::EnumObjects
author: windows-sdk-content
description: The EnumObjects method retrieves an interface that is used to enumerate the immediate child objects of an object. It has an optional filter that can enumerate objects with specific properties.
old-location: wpdsdk\iportabledevicecontent_enumobjects.htm
tech.root: wpd_sdk
ms.assetid: 72526019-58c9-4a18-a925-e0a900f3e35a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumObjects, EnumObjects method [Windows Portable Devices SDK], EnumObjects method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],EnumObjects method, IPortableDeviceContent.EnumObjects, IPortableDeviceContent::EnumObjects, IPortableDeviceContentEnumObjects, portabledeviceapi/IPortableDeviceContent::EnumObjects, wpdsdk.iportabledevicecontent_enumobjects
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceContent.EnumObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceContent::EnumObjects


## -description


The <b>EnumObjects</b> method retrieves an interface that is used to enumerate the immediate child objects of an object. It has an optional filter that can enumerate objects with specific properties.
      


## -parameters




### -param dwFlags [in]

Currently ignored; specify zero.
          


### -param pszParentObjectID [in]

Pointer to a null-terminated string that specifies the ID of the parent. This can be an empty string (but not a <b>NULL</b> pointer) or the defined constant <b>WPD_DEVICE_OBJECT_ID</b> to indicate the device root.
          


### -param pFilter [in]

This parameter is ignored and should be set to <b>NULL</b>.
          


### -param ppEnum [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/0e9a65cc-819c-494e-9c7c-8f5fec78a2ee">IEnumPortableDeviceObjectIDs</a> interface that is used to enumerate the objects that are found. The caller must release this interface when it is done with it.
          


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
 




## -see-also




<a href="https://msdn.microsoft.com/86782a09-4fca-4ae0-beaf-296069e061dc">Enumerating Content</a>



<a href="https://msdn.microsoft.com/4af4201c-d3f6-4630-91ec-6509c51871a5">Enumerating Service Content</a>



<a href="https://msdn.microsoft.com/72526019-58c9-4a18-a925-e0a900f3e35a">IPortableDeviceContent</a>



<a href="wpdsdk.iportabledevicecontent">IPortableDeviceContent Interface</a>
 

 

