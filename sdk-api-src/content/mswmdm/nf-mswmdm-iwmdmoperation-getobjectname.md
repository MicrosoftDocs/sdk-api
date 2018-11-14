---
UID: NF:mswmdm.IWMDMOperation.GetObjectName
title: IWMDMOperation::GetObjectName
author: windows-sdk-content
description: Windows Media Device Manager calls GetObjectName before an object is written to the device in order to know what it should be named on the device.
old-location: wmdm\iwmdmoperation_getobjectname.htm
tech.root: WMDM
ms.assetid: e66882ec-2fcf-44c7-b78a-a3b55d9e9ec4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetObjectName, GetObjectName method [windows Media Device Manager], GetObjectName method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],GetObjectName method, IWMDMOperation.GetObjectName, IWMDMOperation::GetObjectName, IWMDMOperationGetObjectName, mswmdm/IWMDMOperation::GetObjectName, wmdm.iwmdmoperation_getobjectname
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
 - IWMDMOperation.GetObjectName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IWMDMOperation.GetObjectName
: 
---

# IWMDMOperation::GetObjectName


## -description



Windows Media Device Manager calls <b>GetObjectName</b> before an object is written to the device in order to know what it should be named on the device.




## -parameters




### -param pwszName [out]

Pointer to a wide-character null-terminated string that specifies the object name. The name should include a file extension, if required. Windows Media Device Manager allocates and releases this buffer. <i>nMaxChars</i> specifies the maximum number of characters, including the terminating null character.


### -param nMaxChars [in]

Integer specifying the number of characters in <i>pwszName</i>, including the terminating null character.


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



This method is only called if the application did not specify the name as a parameter in the <b>Insert</b> method.




## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/d15b9cb0-6984-401e-9f81-97d0aae17b76">IWMDMOperation::SetObjectName</a>
 

 

