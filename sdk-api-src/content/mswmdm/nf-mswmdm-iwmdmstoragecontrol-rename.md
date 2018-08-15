---
UID: NF:mswmdm.IWMDMStorageControl.Rename
title: IWMDMStorageControl::Rename
author: windows-sdk-content
description: The Rename method renames the current storage.
old-location: wmdm\iwmdmstoragecontrol_rename.htm
old-project: WMDM
ms.assetid: 06cd302b-7876-4256-aa75-27127eb45ac9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMDMStorageControl interface [windows Media Device Manager],Rename method, IWMDMStorageControl.Rename, IWMDMStorageControl::Rename, IWMDMStorageControlRename, Rename, Rename method [windows Media Device Manager], Rename method [windows Media Device Manager],IWMDMStorageControl interface, mswmdm/IWMDMStorageControl::Rename, wmdm.iwmdmstoragecontrol_rename
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorageControl.Rename
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorageControl::Rename


## -description



The <b>Rename</b> method renames the current storage.




## -parameters




### -param fuMode [in]

Processing mode used for the <b>Rename</b> operation. Specify exactly one of the following two modes. If both modes are specified, block mode is used.

<table>
<tr>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode processing. The call will return immediately, and the operation is performed in a background thread.</td>
</tr>
</table>
 


### -param pwszNewName [in]

Pointer to a wide-character null-terminated string specifying the new name.


### -param pProgress [in]

Optional pointer to an <b>IWMDMProgress</b> interface that has been implemented by the application to track the progress of the action.


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

If an application uses WMDM_MODE_THREAD and passes a non-null <i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the read operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an End notification. Failure to do this will result in access violations.




## -see-also




<a href="https://msdn.microsoft.com/18445ba5-6c91-4b4c-8f9b-b9d94fd96155">IWMDMDevice::GetStatus</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/1387a82f-e320-402a-b3c9-2f28550c4caf">IWMDMStorage::GetName</a>



<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>
 

 

