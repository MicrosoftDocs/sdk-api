---
UID: NF:vds.IVdsVDisk.Open
title: IVdsVDisk::Open
author: windows-sdk-content
description: Opens a handle to the specified virtual disk file and returns an IVdsOpenVDisk interface pointer to the object that represents the opened handle.
old-location: base\ivdsvdisk_open.htm
tech.root: vds
ms.assetid: e633f934-8f2d-4614-b34c-87bb74ebf385
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVdsVDisk interface,Open method, IVdsVDisk.Open, IVdsVDisk::Open, Open, Open method, Open method,IVdsVDisk interface, base.ivdsvdisk_open, vds/IVdsVDisk::Open
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVDisk.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVDisk::Open


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Opens a handle to the specified virtual disk file and returns an <a href="https://msdn.microsoft.com/3d5f080f-3e83-437e-8cbc-9730988f5dcc">IVdsOpenVDisk</a> interface pointer to the object that represents the opened handle.


## -parameters




### -param AccessMask [in]

A bitmask of <a href="https://msdn.microsoft.com/2b1f02ab-dc32-4af1-880b-73e7db8602be">VIRTUAL_DISK_ACCESS_MASK</a> flags specifying the access rights to be applied to the opened virtual disk.


### -param Flags [in]

A bitmask of <a href="https://msdn.microsoft.com/edc7d3ad-23a0-4e7a-82d5-8ac4df785f35">OPEN_VIRTUAL_DISK_FLAG</a> flags specifying how the virtual disk is to be opened.


### -param ReadWriteDepth [in]

The number of stores (backing files), beginning with the child, of the backing store chain to open read/write. The remaining stores in the differencing chain will be opened read-only. (This is necessary for merge operations to succeed.)


### -param ppOpenVDisk [out]

A pointer to a variable that receives an <a href="https://msdn.microsoft.com/3d5f080f-3e83-437e-8cbc-9730988f5dcc">IVdsOpenVDisk</a> interface pointer to the newly created object that represents the handle opened to the virtual disk object. Callers must release the interface pointer when it is no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The method completed successfully.

</td>
</tr>
</table>
 




## -remarks



Applications must initialize process-wide security by calling the <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> function. The <i>dwImpLevel</i> parameter should be set to <b>RPC_C_IMP_LEVEL_IMPERSONATE</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>These actions are not required until Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a>
 

 

