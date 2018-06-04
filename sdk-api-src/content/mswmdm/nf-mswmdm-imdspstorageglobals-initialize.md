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

# IMDSPStorageGlobals::Initialize


## -description



The <b>Initialize</b> method formats the storage medium. This method is optional. However, this method should be implemented if the device supports this functionality. If this method is not implemented, <a href="https://msdn.microsoft.com/83204c04-503d-4687-8a4d-3c95a6def8d1">IMDSPStorageGlobals::GetCapabilities</a> must return WMDM_STORAGECAP_NOT_INITIALIZABLE in addition to any other flags. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -parameters




### -param fuMode [in]

Mode used to initialize the medium. Specify exactly one of the following two modes. If both modes are specified, block mode is used.

<table>
<tr>
<th>
                  Mode
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode processing. The call is not returned until the operation is finished.</td>
</tr>
<tr>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode processing. The call returns immediately and the operation is performed in a background thread.</td>
</tr>
</table>
 


### -param pProgress [in]

Pointer to an <b>IWMDMProgress</b> interface implemented by an application to track the progress of the formatting operation. This parameter can be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



If WMDM_MODE_BLOCK is specified, <b>Initialize</b> does not return until formatting is finished. If the WMDM_MODE_THREAD is specified, the call returns immediately and the caller can use the <b>IMDSPStorageGlobals::GetStatus</b> method to track the initializing operation.




## -see-also




<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/83204c04-503d-4687-8a4d-3c95a6def8d1">IMDSPStorageGlobals::GetCapabilities</a>



<a href="https://msdn.microsoft.com/572b5de6-62d7-450f-851f-d09b1864a86c">IMDSPStorageGlobals::GetStatus</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>
 

 

