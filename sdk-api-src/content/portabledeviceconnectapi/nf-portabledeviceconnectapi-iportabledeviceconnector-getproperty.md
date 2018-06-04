---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPortableDeviceConnector::GetProperty


## -description


The <b>GetProperty</b> method retrieves a property for the given MTP/Bluetooth Bus Enumerator device.


## -parameters




### -param pPropertyKey [in]

A pointer to a property key for the requested property.


### -param pPropertyType [out]

A pointer to a property type.


### -param ppData [out]

The address of a pointer to the property data.


### -param pcbData [out]

A pointer to the size (in bytes) of the property data.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The specified property key is not supported.

</td>
</tr>
</table>
 




## -remarks



The properties retrieved by this method are set on the device node. An example property key is <b>DEVPKEY_MTPBTH_IsConnected</b>, which indicates whether the device is currently connected.

Valid values for the <i>pPropertyType</i> parameter are system-defined base data types of the unified device property model. The data-type names start with the prefix <b>DEVPROP_TYPE_</b>.

Once the application no longer needs the property data specified by the <i>ppData</i> parameter, it must call <b>CoTaskMemAlloc</b> to free this data.


#### Examples

The following example shows how to read the DEVPKEY_MTPBTH_IsConnected property for a paired MTP/Bluetooth device.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;devpkey.h&gt;
#include &lt;PortableDeviceConnectAPI.h&gt;
HRESULT IsDeviceConnected(
__in  IPortableDeviceConnector* pDevice, 
__out BOOL* pIsConnected)
{
    DEVPROPTYPE     typeGet;
    BYTE*           pDataGet;
    UINT32          cbDataGet;
    *pbIsConnected = FALSE; 
    HRESULT hr = pDevice -&gt;GetProperty(&amp;DEVPKEY_MTPBTH_IsConnected,
                                       &amp;typeGet,
                                       &amp;pDataGet,
                                       &amp;cbDataGet);
    if (SUCCEEDED(hr))
    {
        DEVPROP_BOOLEAN bIsConnected = *((DEVPROP_BOOLEAN*)pDataGet);
        if (bIsConnected == DEVPROP_TRUE)
        {
            * pIsConnected = TRUE;
        }
        // Release memory allocated by GetProperty
        CoTaskMemFree(pDataGet);
    }  
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a>
 

 

