---
UID: NF:mfidl.IMFShutdown.GetShutdownStatus
title: IMFShutdown::GetShutdownStatus (mfidl.h)
description: Queries the status of an earlier call to the IMFShutdown::Shutdown method.
helpviewer_keywords: ["8cf5f5f3-a3ad-4745-87e8-764ed118477a","GetShutdownStatus","GetShutdownStatus method [Media Foundation]","GetShutdownStatus method [Media Foundation]","IMFShutdown interface","IMFShutdown interface [Media Foundation]","GetShutdownStatus method","IMFShutdown.GetShutdownStatus","IMFShutdown::GetShutdownStatus","mf.imfshutdown_getshutdownstatus","mfidl/IMFShutdown::GetShutdownStatus"]
old-location: mf\imfshutdown_getshutdownstatus.htm
tech.root: mf
ms.assetid: 8cf5f5f3-a3ad-4745-87e8-764ed118477a
ms.date: 12/05/2018
ms.keywords: 8cf5f5f3-a3ad-4745-87e8-764ed118477a, GetShutdownStatus, GetShutdownStatus method [Media Foundation], GetShutdownStatus method [Media Foundation],IMFShutdown interface, IMFShutdown interface [Media Foundation],GetShutdownStatus method, IMFShutdown.GetShutdownStatus, IMFShutdown::GetShutdownStatus, mf.imfshutdown_getshutdownstatus, mfidl/IMFShutdown::GetShutdownStatus
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFShutdown::GetShutdownStatus
 - mfidl/IMFShutdown::GetShutdownStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFShutdown.GetShutdownStatus
---

# IMFShutdown::GetShutdownStatus


## -description

Queries the status of an earlier call to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">IMFShutdown::Shutdown</a> method.

## -parameters

### -param pStatus [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfshutdown_status">MFSHUTDOWN_STATUS</a> enumeration.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">Shutdown</a> method has not been called on this object.
              

</td>
</tr>
</table>

## -remarks

Until <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">Shutdown</a> is called, the <b>GetShutdownStatus</b> method returns <b>MF_E_INVALIDREQUEST</b>.

If an object's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">Shutdown</a> method is asynchronous, <i>pStatus</i> might receive the value <b>MFSHUTDOWN_INITIATED</b>. When the object is completely shut down, <i>pStatus</i> receives the value <b>MFSHUTDOWN_COMPLETED</b>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a>