---
UID: NF:portabledeviceapi.IPortableDeviceContent.Transfer
title: IPortableDeviceContent::Transfer (portabledeviceapi.h)
description: The Transfer method retrieves an interface that is used to read from or write to the content data of an existing object resource.helpviewer_keywords: ["IPortableDeviceContent interface [Windows Portable Devices SDK]","Transfer method","IPortableDeviceContent.Transfer","IPortableDeviceContent::Transfer","IPortableDeviceContentTransfer","Transfer","Transfer method [Windows Portable Devices SDK]","Transfer method [Windows Portable Devices SDK]","IPortableDeviceContent interface","portabledeviceapi/IPortableDeviceContent::Transfer","wpdsdk.iportabledevicecontent_transfer"]
old-location: wpdsdk\iportabledevicecontent_transfer.htm
tech.root: wpd_sdk
ms.assetid: 52fd2ca7-56ba-4e7a-9dcc-5b28f344c1df
ms.date: 12/05/2018
ms.keywords: IPortableDeviceContent interface [Windows Portable Devices SDK],Transfer method, IPortableDeviceContent.Transfer, IPortableDeviceContent::Transfer, IPortableDeviceContentTransfer, Transfer, Transfer method [Windows Portable Devices SDK], Transfer method [Windows Portable Devices SDK],IPortableDeviceContent interface, portabledeviceapi/IPortableDeviceContent::Transfer, wpdsdk.iportabledevicecontent_transfer
f1_keywords:
- portabledeviceapi/IPortableDeviceContent.Transfer
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceContent::Transfer


## -description


The <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-move">Transfer</a> method retrieves an interface that is used to read from or write to the content data of an existing object resource.
      


## -parameters




### -param ppResources [out]

Address of a variable that receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceresources">IPortableDeviceResources</a> interface that is used to modify an object's resources. The caller must release this interface when it is done with it.
          


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

For an example of how to use this method, see <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/adding-a-resource-to-an-object">Adding a Resource to an Object</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/adding-a-resource-to-an-object">Adding a Resource to an Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>
 

 

