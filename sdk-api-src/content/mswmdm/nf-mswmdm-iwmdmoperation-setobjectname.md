---
UID: NF:mswmdm.IWMDMOperation.SetObjectName
title: IWMDMOperation::SetObjectName (mswmdm.h)
description: The SetObjectName method assigns a name to the content being read or written. This method is currently not called by Windows Media Device Manager.
helpviewer_keywords: ["IWMDMOperation interface [windows Media Device Manager]","SetObjectName method","IWMDMOperation.SetObjectName","IWMDMOperation::SetObjectName","IWMDMOperationSetObjectName","SetObjectName","SetObjectName method [windows Media Device Manager]","SetObjectName method [windows Media Device Manager]","IWMDMOperation interface","mswmdm/IWMDMOperation::SetObjectName","wmdm.iwmdmoperation_setobjectname"]
old-location: wmdm\iwmdmoperation_setobjectname.htm
tech.root: WMDM
ms.assetid: d15b9cb0-6984-401e-9f81-97d0aae17b76
ms.date: 12/05/2018
ms.keywords: IWMDMOperation interface [windows Media Device Manager],SetObjectName method, IWMDMOperation.SetObjectName, IWMDMOperation::SetObjectName, IWMDMOperationSetObjectName, SetObjectName, SetObjectName method [windows Media Device Manager], SetObjectName method [windows Media Device Manager],IWMDMOperation interface, mswmdm/IWMDMOperation::SetObjectName, wmdm.iwmdmoperation_setobjectname
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
 - IWMDMOperation::SetObjectName
 - mswmdm/IWMDMOperation::SetObjectName
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
 - IWMDMOperation.SetObjectName
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

<a href="/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname">IWMDMOperation::GetObjectName</a>