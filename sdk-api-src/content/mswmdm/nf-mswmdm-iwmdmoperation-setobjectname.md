---
UID: NF:mswmdm.IWMDMOperation.SetObjectName
title: IWMDMOperation::SetObjectName
author: windows-sdk-content
description: The SetObjectName method assigns a name to the content being read or written. This method is currently not called by Windows Media Device Manager.
old-location: wmdm\iwmdmoperation_setobjectname.htm
old-project: WMDM
ms.assetid: d15b9cb0-6984-401e-9f81-97d0aae17b76
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMDMOperation interface [windows Media Device Manager],SetObjectName method, IWMDMOperation.SetObjectName, IWMDMOperation::SetObjectName, IWMDMOperationSetObjectName, SetObjectName, SetObjectName method [windows Media Device Manager], SetObjectName method [windows Media Device Manager],IWMDMOperation interface, mswmdm/IWMDMOperation::SetObjectName, wmdm.iwmdmoperation_setobjectname
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMDMOperation.SetObjectName
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMOperation::SetObjectName


## -description



The <b>SetObjectName</b> method assigns a name to the content being read or written. This method is currently not called by Windows Media Device Manager.




## -parameters




### -param pwszName [in]

Pointer to a wide-character null-terminated string specifying the object name.


### -param nMaxChars [in]

Integer specifying the maximum number of characters that this string can hold.


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



This method is called after <b>BeginRead</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/e66882ec-2fcf-44c7-b78a-a3b55d9e9ec4">IWMDMOperation::GetObjectName</a>
 

 

