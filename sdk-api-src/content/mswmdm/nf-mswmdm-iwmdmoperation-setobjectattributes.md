---
UID: NF:mswmdm.IWMDMOperation.SetObjectAttributes
title: IWMDMOperation::SetObjectAttributes (mswmdm.h)
description: The SetObjectAttributes method specifies the file attributes. This method is currently not called by Windows Media Device Manager.
helpviewer_keywords: ["IWMDMOperation interface [windows Media Device Manager]","SetObjectAttributes method","IWMDMOperation.SetObjectAttributes","IWMDMOperation::SetObjectAttributes","IWMDMOperationSetObjectAttributes","SetObjectAttributes","SetObjectAttributes method [windows Media Device Manager]","SetObjectAttributes method [windows Media Device Manager]","IWMDMOperation interface","mswmdm/IWMDMOperation::SetObjectAttributes","wmdm.iwmdmoperation_setobjectattributes"]
old-location: wmdm\iwmdmoperation_setobjectattributes.htm
tech.root: WMDM
ms.assetid: 0ee2eabe-c20d-48fe-96f4-cb4143869462
ms.date: 12/05/2018
ms.keywords: IWMDMOperation interface [windows Media Device Manager],SetObjectAttributes method, IWMDMOperation.SetObjectAttributes, IWMDMOperation::SetObjectAttributes, IWMDMOperationSetObjectAttributes, SetObjectAttributes, SetObjectAttributes method [windows Media Device Manager], SetObjectAttributes method [windows Media Device Manager],IWMDMOperation interface, mswmdm/IWMDMOperation::SetObjectAttributes, wmdm.iwmdmoperation_setobjectattributes
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
 - IWMDMOperation::SetObjectAttributes
 - mswmdm/IWMDMOperation::SetObjectAttributes
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
 - IWMDMOperation.SetObjectAttributes
---

# IWMDMOperation::SetObjectAttributes


## -description

The <b>SetObjectAttributes</b> method specifies the file attributes. This method is currently not called by Windows Media Device Manager.

## -parameters

### -param dwAttributes [in]

<b>DWORD</b> specifying the object attributes as defined in the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes">IWMDMStorage::SetAttributes</a> method.

### -param pFormat [in]

Pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structure specifying the format for files with audio data attributes. If the file contains audio data, this parameter should be filled.

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

Audio attributes include the number of samples per second, the number of bytes per sample, and so on.

## -see-also

<a href="/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes">IWMDMOperation::GetObjectAttributes</a>