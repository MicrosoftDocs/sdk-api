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

# _NTMS_MEDIAPOOLINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_MEDIAPOOLINFORMATION</b> structure defines the properties specific to a media pool object.


## -struct-fields




### -field PoolType

NTMS supports the following media pool types. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_UNKNOWN"></a><a id="ntms_pooltype_unknown"></a><dl>
<dt><b>NTMS_POOLTYPE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Unknown pool type.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_SCRATCH"></a><a id="ntms_pooltype_scratch"></a><dl>
<dt><b>NTMS_POOLTYPE_SCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Media that is available to other applications.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_FOREIGN"></a><a id="ntms_pooltype_foreign"></a><dl>
<dt><b>NTMS_POOLTYPE_FOREIGN</b></dt>
</dl>
</td>
<td width="60%">
Media that has been written to and does not contain a recognizable on-media identifier label-type or label ID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_IMPORT"></a><a id="ntms_pooltype_import"></a><dl>
<dt><b>NTMS_POOLTYPE_IMPORT</b></dt>
</dl>
</td>
<td width="60%">
Media that has been written to, has a recognizable on-media identifier label type but an unrecognizable label ID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_APPLICATION"></a><a id="ntms_pooltype_application"></a><dl>
<dt><b>NTMS_POOLTYPE_APPLICATION</b></dt>
</dl>
</td>
<td width="60%">
Media pool created by an application. One or more application media pools can be created per system.

</td>
</tr>
</table>
 


### -field MediaType

Single media type that makes up each media pool.


### -field Parent

Parent media pool or <b>NULL</b>.


### -field AllocationPolicy

Bit field indicating action at allocation time. This member is writable. This can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_ALLOCATE_FROMSCRATCH"></a><a id="ntms_allocate_fromscratch"></a><dl>
<dt><b>NTMS_ALLOCATE_FROMSCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Draw media from free if none is available in the pool. The default is not to draw from free.

</td>
</tr>
</table>
 


### -field DeallocationPolicy

Bit field indicating action at deallocation time. This member is writable. This can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DEALLOCATE_TOSCRATCH"></a><a id="ntms_deallocate_toscratch"></a><dl>
<dt><b>NTMS_DEALLOCATE_TOSCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Return media to free when available. The default is not to return to free.

</td>
</tr>
</table>
 


### -field dwMaxAllocates

Number of times the medium can be allocated and deallocated. This member is writable.


### -field dwNumberOfPhysicalMedia

Number of physical media in this media pool.


### -field dwNumberOfLogicalMedia

Number of logical media in this media pool.


### -field dwNumberOfMediaPools

Number of media pools in this media pool.


## -remarks



The 
<b>NTMS_MEDIAPOOLINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

