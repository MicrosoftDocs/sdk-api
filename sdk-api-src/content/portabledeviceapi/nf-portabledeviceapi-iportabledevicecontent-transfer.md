---
UID: NF:portabledeviceapi.IPortableDeviceContent.Transfer
title: IPortableDeviceContent::Transfer
author: windows-sdk-content
description: The Transfer method retrieves an interface that is used to read from or write to the content data of an existing object resource.
old-location: wpdsdk\iportabledevicecontent_transfer.htm
tech.root: wpd_sdk
ms.assetid: 52fd2ca7-56ba-4e7a-9dcc-5b28f344c1df
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPortableDeviceContent interface [Windows Portable Devices SDK],Transfer method, IPortableDeviceContent.Transfer, IPortableDeviceContent::Transfer, IPortableDeviceContentTransfer, Transfer, Transfer method [Windows Portable Devices SDK], Transfer method [Windows Portable Devices SDK],IPortableDeviceContent interface, portabledeviceapi/IPortableDeviceContent::Transfer, wpdsdk.iportabledevicecontent_transfer
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
 - IPortableDeviceContent.Transfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceContent::Transfer


## -description


The <a href="https://msdn.microsoft.com/938a6a06-31c5-44d1-b87b-a108995ae9a1">Transfer</a> method retrieves an interface that is used to read from or write to the content data of an existing object resource.
      


## -parameters




### -param ppResources [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/fce2d6db-13f0-4c1d-ba55-16139c6acbb7">IPortableDeviceResources</a> interface that is used to modify an object's resources. The caller must release this interface when it is done with it.
          


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



This method is typically used to read from an existing object.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/81476f50-5ea0-4e02-9e38-2b1dfcc32c4f">Adding a Resource to an Object</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/81476f50-5ea0-4e02-9e38-2b1dfcc32c4f">Adding a Resource to an Object</a>



<a href="wpdsdk.iportabledevicecontent">IPortableDeviceContent Interface</a>
 

 

