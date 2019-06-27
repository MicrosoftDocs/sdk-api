---
UID: NF:mswmdm.IWMDMOperation.SetObjectTotalSize
title: IWMDMOperation::SetObjectTotalSize (mswmdm.h)
author: windows-sdk-content
description: The SetObjectTotalSize method assigns the total size in bytes of an object. This method is currently not called by Windows Media Device Manager.
old-location: wmdm\iwmdmoperation_setobjecttotalsize.htm
tech.root: WMDM
ms.assetid: 009716e8-6a4e-4373-9a7c-69dad815e743
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMOperation interface [windows Media Device Manager],SetObjectTotalSize method, IWMDMOperation.SetObjectTotalSize, IWMDMOperation::SetObjectTotalSize, IWMDMOperationSetObjectTotalSize, SetObjectTotalSize, SetObjectTotalSize method [windows Media Device Manager], SetObjectTotalSize method [windows Media Device Manager],IWMDMOperation interface, mswmdm/IWMDMOperation::SetObjectTotalSize, wmdm.iwmdmoperation_setobjecttotalsize
ms.topic: method
f1_keywords: 
 - "mswmdm/IWMDMOperation.SetObjectTotalSize"
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
 - IWMDMOperation.SetObjectTotalSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMOperation::SetObjectTotalSize


## -description



The <b>SetObjectTotalSize</b> method assigns the total size in bytes of an object. This method is currently not called by Windows Media Device Manager.




## -parameters




### -param dwSize [in]

<b>DWORD</b> specifying the low-order bits of the object size, in bytes.


### -param dwSizeHigh [in]

<b>DWORD</b> specifying the high-order bits of the object size, in bytes.


## -returns



The application should return one of the following <b>HRESULT</b> values.

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
The read operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The read operation should be cancelled without finishing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred, and the read operation should be cancelled without finishing.

</td>
</tr>
</table>
 




## -remarks



This method is called after <b>SetObjectAttributes</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize">IWMDMOperation::GetObjectTotalSize</a>
 

 

