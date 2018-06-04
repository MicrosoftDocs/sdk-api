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

# _STORAGE_WRITE_CACHE_PROPERTY structure


## -description


Used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> control code to retrieve information about a device's write cache property.


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.


### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.


### -field WriteCacheType

A value from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568044">WRITE_CACHE_TYPE</a> enumeration 
      that indicates the current write cache type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WriteCacheTypeUnknown"></a><a id="writecachetypeunknown"></a><a id="WRITECACHETYPEUNKNOWN"></a><dl>
<dt><b>WriteCacheTypeUnknown</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system cannot report the type of the write cache.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteCacheTypeNone"></a><a id="writecachetypenone"></a><a id="WRITECACHETYPENONE"></a><dl>
<dt><b>WriteCacheTypeNone</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The device does not have a write cache.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteCacheTypeWriteBack"></a><a id="writecachetypewriteback"></a><a id="WRITECACHETYPEWRITEBACK"></a><dl>
<dt><b>WriteCacheTypeWriteBack</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The device has a write-back cache.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteCacheTypeWriteThrough"></a><a id="writecachetypewritethrough"></a><a id="WRITECACHETYPEWRITETHROUGH"></a><dl>
<dt><b>WriteCacheTypeWriteThrough</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The device has a write-through cache.

</td>
</tr>
</table>
 


### -field WriteCacheEnabled

A value from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568042">WRITE_CACHE_ENABLE</a> enumeration 
      that indicates whether the write cache is enabled.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WriteCacheEnableUnknown"></a><a id="writecacheenableunknown"></a><a id="WRITECACHEENABLEUNKNOWN"></a><dl>
<dt><b>WriteCacheEnableUnknown</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system cannot report whether the device's write cache is enabled or disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteCacheDisabled"></a><a id="writecachedisabled"></a><a id="WRITECACHEDISABLED"></a><dl>
<dt><b>WriteCacheDisabled</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The device's write cache is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteCacheEnabled"></a><a id="writecacheenabled"></a><a id="WRITECACHEENABLED"></a><dl>
<dt><b>WriteCacheEnabled</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The device's write cache is enabled.

</td>
</tr>
</table>
 


### -field WriteCacheChangeable

A value from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568039">WRITE_CACHE_CHANGE</a> enumeration that 
      indicates whether if the host can change the write cache characteristics.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WriteCacheChangeUnknown"></a><a id="writecachechangeunknown"></a><a id="WRITECACHECHANGEUNKNOWN"></a><dl>
<dt><b>WriteCacheChangeUnknown</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system cannot report the write cache change capability of the device.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteCacheNotChangeable"></a><a id="writecachenotchangeable"></a><a id="WRITECACHENOTCHANGEABLE"></a><dl>
<dt><b>WriteCacheNotChangeable</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Host software cannot change the characteristics of the device's write cache 

</td>
</tr>
<tr>
<td width="40%"><a id="WriteCacheChangeable"></a><a id="writecachechangeable"></a><a id="WRITECACHECHANGEABLE"></a><dl>
<dt><b>WriteCacheChangeable</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Host software can change the characteristics of the device's write cache 

</td>
</tr>
</table>
 


### -field WriteThroughSupported

A value from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568047">WRITE_THROUGH</a> enumeration that indicates whether the device supports write-through caching.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WriteThroughUnknown"></a><a id="writethroughunknown"></a><a id="WRITETHROUGHUNKNOWN"></a><dl>
<dt><b>WriteThroughUnknown</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Indicates that no information is available concerning the write-through capabilities of the device.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteThroughNotSupported"></a><a id="writethroughnotsupported"></a><a id="WRITETHROUGHNOTSUPPORTED"></a><dl>
<dt><b>WriteThroughNotSupported</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Indicates that the device does not support write-through operations.

</td>
</tr>
<tr>
<td width="40%"><a id="WriteThroughSupported"></a><a id="writethroughsupported"></a><a id="WRITETHROUGHSUPPORTED"></a><dl>
<dt><b>WriteThroughSupported</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Indicates that the device supports write-through operations.

</td>
</tr>
</table>
 


### -field FlushCacheSupported

A <b>BOOLEAN</b> value that indicates whether the device allows host software to 
      flush the device cache. If <b>TRUE</b>, the device allows host software to flush the device 
      cache. If <b>FALSE</b>, host software cannot flush the device cache.


### -field UserDefinedPowerProtection

A <b>BOOLEAN</b> value that indicates whether a user can configure the device's power 
      protection characteristics in the registry. If <b>TRUE</b>, a user can configure the device's 
      power protection characteristics in the registry. If <b>FALSE</b>, the user cannot configure 
      the device's power protection characteristics in the registry.


### -field NVCacheEnabled

A <b>BOOLEAN</b> value that indicates whether the device has a battery backup for the 
      write cache. If <b>TRUE</b>, the device has a battery backup for the write cache. If 
      <b>FALSE</b>, the device does not have a battery backup for the writer cache.


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>
 

 

