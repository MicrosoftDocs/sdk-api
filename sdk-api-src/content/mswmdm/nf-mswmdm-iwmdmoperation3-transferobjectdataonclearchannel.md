---
UID: NF:mswmdm.IWMDMOperation3.TransferObjectDataOnClearChannel
title: IWMDMOperation3::TransferObjectDataOnClearChannel (mswmdm.h)
description: The TransferObjectDataOnClearChannel method is a more efficient implementation of IWMDMOperation::TransferObjectData.
helpviewer_keywords: ["IWMDMOperation3 interface [windows Media Device Manager]","TransferObjectDataOnClearChannel method","IWMDMOperation3.TransferObjectDataOnClearChannel","IWMDMOperation3::TransferObjectDataOnClearChannel","IWMDMOperation3TransferObjectDataOnClearChannel","TransferObjectDataOnClearChannel","TransferObjectDataOnClearChannel method [windows Media Device Manager]","TransferObjectDataOnClearChannel method [windows Media Device Manager]","IWMDMOperation3 interface","mswmdm/IWMDMOperation3::TransferObjectDataOnClearChannel","wmdm.iwmdmoperation3__transferobjectdataonclearchannel"]
old-location: wmdm\iwmdmoperation3__transferobjectdataonclearchannel.htm
tech.root: WMDM
ms.assetid: a5cc0151-35c0-4de6-9bb3-f07339c60042
ms.date: 12/05/2018
ms.keywords: IWMDMOperation3 interface [windows Media Device Manager],TransferObjectDataOnClearChannel method, IWMDMOperation3.TransferObjectDataOnClearChannel, IWMDMOperation3::TransferObjectDataOnClearChannel, IWMDMOperation3TransferObjectDataOnClearChannel, TransferObjectDataOnClearChannel, TransferObjectDataOnClearChannel method [windows Media Device Manager], TransferObjectDataOnClearChannel method [windows Media Device Manager],IWMDMOperation3 interface, mswmdm/IWMDMOperation3::TransferObjectDataOnClearChannel, wmdm.iwmdmoperation3__transferobjectdataonclearchannel
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
 - IWMDMOperation3::TransferObjectDataOnClearChannel
 - mswmdm/IWMDMOperation3::TransferObjectDataOnClearChannel
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
 - IWMDMOperation3.TransferObjectDataOnClearChannel
---

# IWMDMOperation3::TransferObjectDataOnClearChannel


## -description

The <b>TransferObjectDataOnClearChannel</b> method is a more efficient implementation of <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>.

## -parameters

### -param pData

Pointer to an unencrypted byte buffer.

### -param pdwSize

Pointer to a variable specifying the buffer size.

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

If the application supports this method, it is called in preference to the <b>TransferObjectData</b>.

See <b>TransferObjectData</b> to learn about the basics of this function. The difference between this method and <b>TransferObjectData</b> is that this method does not require the sender or receiver to encrypt or decrypt data, which requires extra processing time. Licensed content can still be sent using this method, since the content is always encrypted during transport anyway.

If the application supports this method, it is called in preference to the <b>TransferObjectData</b>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3">IWMDMOperation3 Interface</a>