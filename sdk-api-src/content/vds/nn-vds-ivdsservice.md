---
UID: NN:vds.IVdsService
title: IVdsService
author: windows-sdk-content
description: Provides methods to query and interact with VDS.
old-location: base\ivdsservice.htm
old-project: VDS
ms.assetid: 6b081cc8-fe06-427f-b06d-831a1f1fef52
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsService, IVdsService interface [VDS], IVdsService interface [VDS],described, base.ivdsservice, vds/IVdsService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsService
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsService interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and interact with VDS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">Advise</a>
</td>
<td align="left" width="63%">
Registers the caller's <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface with VDS so that the caller receives notifications from the VDS service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93ed7789-be60-422c-be4f-e70e16d26fce">CleanupObsoleteMountPoints</a>
</td>
<td align="left" width="63%">
Updates the registry by removing user-mode paths and mounted folders for volumes that no longer exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91cb21ea-725b-4032-9a60-34c1b42b55d0">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears the service object flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">GetObject</a>
</td>
<td align="left" width="63%">
Returns an object pointer for the identified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves VDS property information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79ef68db-6bc6-40b3-a133-86f00eb70ee3">IsServiceReady</a>
</td>
<td align="left" width="63%">
Indicates the status of VDS initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9e9f8b0-963f-4c57-9553-8b9241317b55">QueryDriveLetters</a>
</td>
<td align="left" width="63%">
Returns the property information of one or more drive letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17dcafc8-8faf-4dc2-af24-7e1ab257201e">QueryFileSystemTypes</a>
</td>
<td align="left" width="63%">
Returns the property information of all the file systems known to VDS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e53b250-0ceb-4a0c-a1ea-11b2686c5b4d">QueryMaskedDisks</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55171eb1-6fec-4651-914c-88d23e8d7849">QueryProviders</a>
</td>
<td align="left" width="63%">
Enumerates all the hardware or software providers known to VDS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d519c3d0-7c5a-4c0c-bad9-2429490f2212">QueryUnallocatedDisks</a>
</td>
<td align="left" width="63%">
Enumerates  all the unallocated disks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c22be0a5-d7ed-4f76-961d-2455ca99f220">Reboot</a>
</td>
<td align="left" width="63%">
Restarts the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d057715c-dfd5-4b69-9e33-c40fb89fa11b">Reenumerate</a>
</td>
<td align="left" width="63%">
Discovers new disks, removed disks, or both.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca6a1143-b5f0-49e5-8505-836c565aabcf">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes disk ownership and layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the service object flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/085d380c-2e09-470a-a23d-704c31535975">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters the caller's  <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface so that the caller no longer receives notifications from the VDS service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85075abe-7fac-40aa-a93e-19d89c0fd760">WaitForServiceReady</a>
</td>
<td align="left" width="63%">
Waits until initialization either completes successfully (or fails) before invoking methods exposed by VDS objects.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae4d18f2-4d50-480c-bc7a-4eec0334707d">Startup and Service Objects</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/9029ebbd-f05d-4317-913d-58c8a0a62886">VDS_SERVICE_PROP</a>
 

 

