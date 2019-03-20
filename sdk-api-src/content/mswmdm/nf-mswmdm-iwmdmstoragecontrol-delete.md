---
UID: NF:mswmdm.IWMDMStorageControl.Delete
title: IWMDMStorageControl::Delete (mswmdm.h)
author: windows-sdk-content
description: The Delete method permanently deletes this storage.
old-location: wmdm\iwmdmstoragecontrol_delete.htm
tech.root: WMDM
ms.assetid: f2b044d2-6386-4c2e-a437-5ebddf827fb4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Delete, Delete method [windows Media Device Manager], Delete method [windows Media Device Manager],IWMDMStorageControl interface, IWMDMStorageControl interface [windows Media Device Manager],Delete method, IWMDMStorageControl.Delete, IWMDMStorageControl::Delete, IWMDMStorageControlDelete, mswmdm/IWMDMStorageControl::Delete, wmdm.iwmdmstoragecontrol_delete
ms.topic: method
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorageControl.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorageControl::Delete


## -description



The <b>Delete</b> method permanently deletes this storage.




## -parameters




### -param fuMode [in]

One or two of the following flags, combined with a bitwise <b>OR</b>. Specify exactly one of the first two modes; the third mode is optional.

<table>
<tr>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode (synchronous) processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode (asynchronous) processing. The call will return immediately, and the operation is performed in a background thread.</td>
</tr>
<tr>
<td>WMDM_MODE_RECURSIVE</td>
<td>If the storage object is a folder, it and its contents, and all subfolders and their contents are deleted.</td>
</tr>
</table>
 

4


### -param pProgress [in]

Optional pointer to an <a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress</a> interface to be used by Windows Media Device Manager to report progress back to the application.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



If the WMDM_MODE_THREAD flag is specified, you should obtain completion status by calling either <a href="https://msdn.microsoft.com/85265eb7-0702-4890-b6cb-b247296fe392">IWMDMProgress2::End2</a> or <a href="https://msdn.microsoft.com/fb09cfa8-1a96-412f-a97a-6cc1638b0c77">IWMDMProgress3::End3</a>. These methods will ensure that the operation is complete and will also return an HRESULT with success or failure information.

When the <b>Delete</b> operation is finished, all references to the deleted object become invalid. The application must release these interfaces and any other interfaces or resources associated with the object.

If an application uses WMDM_MODE_THREAD and passes a non-null <i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the delete operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an End notification. Failure to do this will result in access violations.




## -see-also




<a href="https://msdn.microsoft.com/18445ba5-6c91-4b4c-8f9b-b9d94fd96155">IWMDMDevice::GetStatus</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/cfb6d233-6fc0-4589-9324-f4242798afc5">IWMDMStorageGlobals::GetStatus</a>
 

 

