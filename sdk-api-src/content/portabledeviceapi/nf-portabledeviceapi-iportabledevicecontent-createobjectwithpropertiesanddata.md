---
UID: NF:portabledeviceapi.IPortableDeviceContent.CreateObjectWithPropertiesAndData
title: IPortableDeviceContent::CreateObjectWithPropertiesAndData (portabledeviceapi.h)
description: The CreateObjectWithPropertiesAndData method creates an object with both properties and data on the device.
helpviewer_keywords: ["CreateObjectWithPropertiesAndData","CreateObjectWithPropertiesAndData method [Windows Portable Devices SDK]","CreateObjectWithPropertiesAndData method [Windows Portable Devices SDK]","IPortableDeviceContent interface","IPortableDeviceContent interface [Windows Portable Devices SDK]","CreateObjectWithPropertiesAndData method","IPortableDeviceContent.CreateObjectWithPropertiesAndData","IPortableDeviceContent::CreateObjectWithPropertiesAndData","IPortableDeviceContentCreateObjectWithPropertiesAndData","portabledeviceapi/IPortableDeviceContent::CreateObjectWithPropertiesAndData","wpdsdk.iportabledevicecontent_createobjectwithpropertiesanddata"]
old-location: wpdsdk\iportabledevicecontent_createobjectwithpropertiesanddata.htm
tech.root: wpdsdk
ms.assetid: ea3445cc-69af-40a6-a5a4-695e0f2e1fb6
ms.date: 12/05/2018
ms.keywords: CreateObjectWithPropertiesAndData, CreateObjectWithPropertiesAndData method [Windows Portable Devices SDK], CreateObjectWithPropertiesAndData method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],CreateObjectWithPropertiesAndData method, IPortableDeviceContent.CreateObjectWithPropertiesAndData, IPortableDeviceContent::CreateObjectWithPropertiesAndData, IPortableDeviceContentCreateObjectWithPropertiesAndData, portabledeviceapi/IPortableDeviceContent::CreateObjectWithPropertiesAndData, wpdsdk.iportabledevicecontent_createobjectwithpropertiesanddata
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceContent::CreateObjectWithPropertiesAndData
 - portabledeviceapi/IPortableDeviceContent::CreateObjectWithPropertiesAndData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceContent.CreateObjectWithPropertiesAndData
---

# IPortableDeviceContent::CreateObjectWithPropertiesAndData


## -description

The <b>CreateObjectWithPropertiesAndData</b> method creates an object with both properties and data on the device.

## -parameters

### -param pValues

An <b>IPortableDeviceValues</b> collection of properties to assign to the object. For a list of required and optional properties for an object, see <a href="/windows/desktop/wpd_sdk/requirements-for-objects">Requirements for Objects</a>.

### -param ppData [out]

Address of a variable that receives a pointer to an <b>IStream</b> interface that the application uses to send the object data to the device. The object will not be created on the device until the application sends the data by calling <i>ppData</i>-&gt;<b>Commit</b>. To abandon a data transfer in progress, you can call <i>ppData</i> -&gt; <b>Revert</b>. The caller must release this interface when it is done with it. The underlying object extends both <b>IStream</b> and <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicedatastream">IPortableDeviceDataStream</a>.

### -param pdwOptimalWriteBufferSize [in, out]

An optional <b>DWORD</b> pointer that specifies the optimal buffer size for the application to use when writing the data to <i>ppData</i>. The application can specify <b>TRUE</b> to ignore this.

### -param ppszCookie [in, out]

An optional unique, null-terminated string ID that is used to identify this creation request in the application's implementation of <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceeventcallback">IPortableDeviceEventCallback</a> (if implemented). When the device finishes creating the object, it will send this identifier to the callback function. This identifier allows an application to monitor object creation in a different thread from the one that called <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesonly">CreateObjectWithPropertiesOnly</a>. The SDK allocates this memory, and the caller must release it using <b>CoTaskMemFree</b>.

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

Some objects are only a collection of properties—such as a folder, which is only a collection of pointers to other objects—while other objects are both properties and data—such as an audio file, which contains all the properties and the actual music bits. This method is used to create an object that requires both properties and data. To create a properties-only object, call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesonly">CreateObjectWithPropertiesOnly</a>.
      

Because the object is not created until the application calls <b>Commit</b> on the retrieved <b>IStream</b> <i>ppData</i>, the object will not have an ID until <b>Commit</b> is called on it. <b>Commit</b> is synchronous, so when that method returns successfully, the object will exist on the device.
      

After calling <b>Commit</b> to create the object, call <b>QueryInterface</b> on <i>ppData</i> for <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicedatastream">IPortableDeviceDataStream</a>, and then call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicedatastream-getobjectid">IPortableDeviceDataStream::GetObjectID</a> to get the ID of the newly created object.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/transferring-an-image-or-music-file-to-the-device">Transferring an Image or Music File to the Device</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicedatastream">IPortableDeviceDataStream Interface</a>



<a href="/windows/desktop/wpd_sdk/transferring-an-image-or-music-file-to-the-device">Transferring an Image or Music File to the Device</a>