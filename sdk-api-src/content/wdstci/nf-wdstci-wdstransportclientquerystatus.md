---
UID: NF:wdstci.WdsTransportClientQueryStatus
title: WdsTransportClientQueryStatus function (wdstci.h)
description: Retrieves the current status of an ongoing or complete multicast transmission from the multicast client.
helpviewer_keywords: ["WdsTransportClientQueryStatus","WdsTransportClientQueryStatus function [Windows Deployment Services]","wds.wdstransportclientquerystatus","wdstci/WdsTransportClientQueryStatus"]
old-location: wds\wdstransportclientquerystatus.htm
tech.root: wds
ms.assetid: 405d8575-a6ae-483e-a49a-9281c5e825a7
ms.date: 12/05/2018
ms.keywords: WdsTransportClientQueryStatus, WdsTransportClientQueryStatus function [Windows Deployment Services], wds.wdstransportclientquerystatus, wdstci/WdsTransportClientQueryStatus
req.header: wdstci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsTransportClientQueryStatus
 - wdstci/WdsTransportClientQueryStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdstptc.dll
api_name:
 - WdsTransportClientQueryStatus
---

# WdsTransportClientQueryStatus function


## -description

Retrieves the current status of an ongoing or complete multicast transmission from the multicast client.

## -parameters

### -param hSessionKey [in]

Unique handle returned by the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientinitializesession">WdsTransportClientInitializeSession</a>.

### -param puStatus [out]

The current status of the transfer.  This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_STATUS_IN_PROGRESS</dt>
</dl>
</td>
<td width="60%">
The multicast session is still in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_STATUS_SUCCESS</dt>
</dl>
</td>
<td width="60%">
The multicast session completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_STATUS_FAILURE</dt>
</dl>
</td>
<td width="60%">
The multicast session failed.

</td>
</tr>
</table>

### -param puErrorCode [out]

If puStatus is set to <b>WDS_TRANSPORTCLIENT_STATUS_FAILURE</b>, this field will be set to the error code of the session.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

It is valid to call this function even after a transfer completes as long as the session key has not been closed.