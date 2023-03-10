---
UID: NF:mfidl.MFGetService
title: MFGetService function (mfidl.h)
description: Queries an object for a specified service interface. (MFGetService)
helpviewer_keywords: ["119e9e2f-0e26-4dfc-9c89-156b63a63640","MFGetService","MFGetService function [Media Foundation]","mf.mfgetservice","mfidl/MFGetService"]
old-location: mf\mfgetservice.htm
tech.root: mf
ms.assetid: 119e9e2f-0e26-4dfc-9c89-156b63a63640
ms.date: 12/05/2018
ms.keywords: 119e9e2f-0e26-4dfc-9c89-156b63a63640, MFGetService, MFGetService function [Media Foundation], mf.mfgetservice, mfidl/MFGetService
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetService
 - mfidl/MFGetService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFGetService
---

# MFGetService function


## -description

Queries an object for a specified service interface.

This function is a helper function that wraps the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> method. The function queries the object for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a> interface and, if successful, calls <b>GetService</b> on the object.

## -parameters

### -param punkObject

A pointer to the <b>IUnknown</b> interface of the object to query.

### -param guidService

The service identifier (SID) of the service. For a list of service identifiers, see <a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>.

### -param riid

The interface identifier (IID) of the interface being requested.

### -param ppvObject

Receives the interface pointer. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
The service requested cannot be found in the object represented by <i>punkObject</i>.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
