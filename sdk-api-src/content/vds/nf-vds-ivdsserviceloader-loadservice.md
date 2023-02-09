---
UID: NF:vds.IVdsServiceLoader.LoadService
title: IVdsServiceLoader::LoadService (vds.h)
description: Launches VDS on the specified computer and returns a pointer to the service object.
helpviewer_keywords: ["IVdsServiceLoader interface [VDS]","LoadService method","IVdsServiceLoader.LoadService","IVdsServiceLoader::LoadService","LoadService","LoadService method [VDS]","LoadService method [VDS]","IVdsServiceLoader interface","base.ivdsserviceloader_loadservice","vds/IVdsServiceLoader::LoadService"]
old-location: base\ivdsserviceloader_loadservice.htm
tech.root: base
ms.assetid: 26bb0a1f-37ad-4bb0-af6c-1063c5ccdc0f
ms.date: 12/05/2018
ms.keywords: IVdsServiceLoader interface [VDS],LoadService method, IVdsServiceLoader.LoadService, IVdsServiceLoader::LoadService, LoadService, LoadService method [VDS], LoadService method [VDS],IVdsServiceLoader interface, base.ivdsserviceloader_loadservice, vds/IVdsServiceLoader::LoadService
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsServiceLoader::LoadService
 - vds/IVdsServiceLoader::LoadService
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
 - IVdsServiceLoader.LoadService
---

# IVdsServiceLoader::LoadService


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Launches VDS on the specified computer and returns a pointer to the service object.

## -parameters

### -param pwszMachineName [in]

This parameter must be set to <b>NULL</b>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This parameter contains the name of the host computer. Setting it to <b>NULL</b> causes VDS to be loaded and initialized on the local host.

### -param ppService [out]

The address of an <a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a> interface pointer. Callers must release the interface when it is no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
The service has launched successfully.

</td>
</tr>
</table>

## -remarks

Although <b>S_OK</b> indicates that VDS has launched successfully, the service initialization can be incomplete when the method returns. For this reason, after calling this method, you must call the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-waitforserviceready">IVdsService::WaitForServiceReady</a> method to wait for VDS initialization to complete.

For a code example, see <a href="/windows/desktop/VDS/loading-vds">Loading VDS</a>.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-waitforserviceready">IVdsService::WaitForServiceReady</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsserviceloader">IVdsServiceLoader</a>