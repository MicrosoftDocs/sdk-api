---
UID: NF:wsdclient.IWSDDeviceProxy.Init
title: IWSDDeviceProxy::Init
author: windows-sdk-content
description: Initializes the device proxy, optionally sharing a session with a previously initialized sponsoring device proxy.
old-location: ncd\iwsddeviceproxy_init_method.htm
old-project: WsdApi
ms.assetid: d29212c8-2f29-41cc-ae35-8376ec5f0b7a
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSDDeviceProxy interface,Init method, IWSDDeviceProxy.Init, IWSDDeviceProxy::Init, Init, Init method, Init method,IWSDDeviceProxy interface, ncd.iwsddeviceproxy_init_method, wsdclient/IWSDDeviceProxy::Init
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceProxy.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceProxy::Init


## -description


Initializes the device proxy, optionally sharing a session with a previously initialized sponsoring device proxy.


## -parameters




### -param pszDeviceId [in]

The logical address (ID) of the device.


### -param pDeviceAddress [in]

Reference to an <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> object that contains the device configuration data.


### -param pszLocalId [in]

The logical address of the client. The logical address is of the form, urn:uuid:{guid}. Used when the server needs to initiate a connection to the client. 


### -param pContext [in, optional]

Reference to an <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> object that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.


### -param pSponsor [in, optional]

Reference to an <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object that is an optional device with which to share a session and lower layers. 



## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszDeviceId</i> is <b>NULL</b>,  <i>pszLocalId</i> is <b>NULL</b>, or the length in characters of either identifier string exceeds WSD_MAX_TEXT_LENGTH (8192). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



This method is called by <a href="https://msdn.microsoft.com/d432ae9a-cf34-4149-978c-637443a3824f">WSDCreateDeviceProxy</a> and need not normally be called directly by the client code.




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

