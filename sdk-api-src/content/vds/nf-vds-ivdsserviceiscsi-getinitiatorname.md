---
UID: NF:vds.IVdsServiceIscsi.GetInitiatorName
title: IVdsServiceIscsi::GetInitiatorName (vds.h)
description: Returns the iSCSI name of the local initiator service.
helpviewer_keywords: ["GetInitiatorName","GetInitiatorName method [VDS]","GetInitiatorName method [VDS]","IVdsServiceIscsi interface","IVdsServiceIscsi interface [VDS]","GetInitiatorName method","IVdsServiceIscsi.GetInitiatorName","IVdsServiceIscsi::GetInitiatorName","base.ivdsserviceiscsi_getinitiatorname","vds/IVdsServiceIscsi::GetInitiatorName"]
old-location: base\ivdsserviceiscsi_getinitiatorname.htm
tech.root: base
ms.assetid: 34f18293-6254-4f73-a633-642a3cdeaf31
ms.date: 12/05/2018
ms.keywords: GetInitiatorName, GetInitiatorName method [VDS], GetInitiatorName method [VDS],IVdsServiceIscsi interface, IVdsServiceIscsi interface [VDS],GetInitiatorName method, IVdsServiceIscsi.GetInitiatorName, IVdsServiceIscsi::GetInitiatorName, base.ivdsserviceiscsi_getinitiatorname, vds/IVdsServiceIscsi::GetInitiatorName
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsServiceIscsi::GetInitiatorName
 - vds/IVdsServiceIscsi::GetInitiatorName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsServiceIscsi.GetInitiatorName
---

# IVdsServiceIscsi::GetInitiatorName


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the iSCSI name of the local initiator service.

## -parameters

### -param ppwszIscsiName [out]

The address of a pointer to a string. VDS will put a pointer to an initialized string at this location. 
      Callers must free the string by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The name was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppwszIscsiName</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsserviceiscsi">IVdsServiceIscsi</a>