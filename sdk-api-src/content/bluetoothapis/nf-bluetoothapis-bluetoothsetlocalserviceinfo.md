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

# BluetoothSetLocalServiceInfo function


## -description


The 
  <b>BluetoothSetLocalServiceInfo</b> function sets local service information for a specific Bluetooth
  radio.


## -parameters




### -param hRadioIn [in, optional]

A handle of the Bluetooth radio device to specify local service information for. If <b>NULL</b>, 
     <b>BluetoothSetLocalServiceInfo</b> searches for the first available local Bluetooth radio.


### -param pClassGuid [in]

The GUID of the service to expose. This should match the <b>GUID</b> in the server-side INF file.


### -param ulInstance [in]

An instance ID for the device node of the Plug and Play (PnP) ID.


### -param pServiceInfoIn [in]

A pointer to a <a href="https://msdn.microsoft.com/d16fe6f1-4b76-4dbe-825e-e3995d2b4961">BLUETOOTH_LOCAL_SERVICE_INFO</a> structure that describes the local service to
     set.


## -returns



The 
     <b>BluetoothSetLocalServiceInfo</b> function returns the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified Bluetooth radio was not detected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_UNIT</b></dt>
</dl>
</td>
<td width="60%">
No Bluetooth radios were detected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Sufficient resources were not available to complete the operation. You can receive this error
       when more than 100 local physical device objects (PDOs) correspond to Bluetooth services.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PRIVILEGE_NOT_HELD</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the required privileges. See the Remarks section for information about
       how to elevate privileges.

</td>
</tr>
</table>
 




## -remarks



<b>BluetoothSetLocalServiceInfo</b> is a user-mode API that is used only by profile driver developers to
    trigger the installation of a local service that is described by the service <b>GUID</b> in 
    <i>pClassGuid</i>.

<b>BluetoothSetLocalServiceInfo</b> generates a Plug and Play (PnP) device ID in the form of "BTHENUM\{<i>ClassGuid</i>}". For example, "BTHENUM\{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". User-mode applications
    can call 
    <b>BluetoothSetLocalServiceInfo</b> subsequent times with the same service GUID but with a different
    instance ID to create multiple instances of the specified server-side profile.

To use Bluetooth APIs like 
    <b>BluetoothSetLocalServiceInfo</b>, user-mode applications should link with 
    BthProps.lib.

<div class="alert"><b>Warning</b>  The process that calls 
    <b>BluetoothSetLocalServiceInfo</b> must have the <b>SE_LOAD_DRIVER_NAME</b> privilege. A process running in the
    system or an administrator context can elevate its privilege by using the SDK 
    <a href="https://msdn.microsoft.com/334b8ba8-101d-43a1-a8bf-1c7e0448c272">LookupPrivilegeValue</a> and 
    <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> functions. For more information about this see 
    <a href="https://msdn.microsoft.com/2bf2b2df-260c-42a5-9ee9-6db91f304036">Installing a Bluetooth
    Device</a>.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/d16fe6f1-4b76-4dbe-825e-e3995d2b4961">BLUETOOTH_LOCAL_SERVICE_INFO</a> structure is defined in the SDK 
    BluetoothApis.h header file.




## -see-also




<a href="https://msdn.microsoft.com/d16fe6f1-4b76-4dbe-825e-e3995d2b4961">BLUETOOTH_LOCAL_SERVICE_INFO</a>
 

 

