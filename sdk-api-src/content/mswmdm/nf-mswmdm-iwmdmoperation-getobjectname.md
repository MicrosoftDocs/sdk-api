---
UID: NF:mswmdm.IWMDMOperation.GetObjectName
title: IWMDMOperation::GetObjectName (mswmdm.h)
description: Windows Media Device Manager calls GetObjectName before an object is written to the device in order to know what it should be named on the device.
helpviewer_keywords: ["GetObjectName","GetObjectName method [windows Media Device Manager]","GetObjectName method [windows Media Device Manager]","IWMDMOperation interface","IWMDMOperation interface [windows Media Device Manager]","GetObjectName method","IWMDMOperation.GetObjectName","IWMDMOperation::GetObjectName","IWMDMOperationGetObjectName","mswmdm/IWMDMOperation::GetObjectName","wmdm.iwmdmoperation_getobjectname"]
old-location: wmdm\iwmdmoperation_getobjectname.htm
tech.root: WMDM
ms.assetid: e66882ec-2fcf-44c7-b78a-a3b55d9e9ec4
ms.date: 12/05/2018
ms.keywords: GetObjectName, GetObjectName method [windows Media Device Manager], GetObjectName method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],GetObjectName method, IWMDMOperation.GetObjectName, IWMDMOperation::GetObjectName, IWMDMOperationGetObjectName, mswmdm/IWMDMOperation::GetObjectName, wmdm.iwmdmoperation_getobjectname
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMOperation::GetObjectName
 - mswmdm/IWMDMOperation::GetObjectName
dev_langs:
 - c++
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

<a href="/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectname">IWMDMOperation::SetObjectName</a>