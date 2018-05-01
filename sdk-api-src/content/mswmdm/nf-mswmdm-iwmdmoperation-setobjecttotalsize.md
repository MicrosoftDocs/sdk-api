---
UID: NF:mswmdm.IWMDMOperation.SetObjectTotalSize
title: IWMDMOperation::SetObjectTotalSize method
author: windows-driver-content
description: The SetObjectTotalSize method assigns the total size in bytes of an object. This method is currently not called by Windows Media Device Manager.
old-location: wmdm\iwmdmoperation_setobjecttotalsize.htm
old-project: WMDM
ms.assetid: 009716e8-6a4e-4373-9a7c-69dad815e743
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IWMDMOperation, IWMDMOperation interface [windows Media Device Manager], SetObjectTotalSize method, IWMDMOperation::SetObjectTotalSize, IWMDMOperationSetObjectTotalSize, SetObjectTotalSize method [windows Media Device Manager], SetObjectTotalSize method [windows Media Device Manager], IWMDMOperation interface, SetObjectTotalSize,IWMDMOperation.SetObjectTotalSize, mswmdm/IWMDMOperation::SetObjectTotalSize, wmdm.iwmdmoperation_setobjecttotalsize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMOperation.SetObjectTotalSize
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMOperation::SetObjectTotalSize method


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




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/50ab01f9-0f38-485e-b7d9-98bc95948427">IWMDMOperation::GetObjectTotalSize</a>
 

 

