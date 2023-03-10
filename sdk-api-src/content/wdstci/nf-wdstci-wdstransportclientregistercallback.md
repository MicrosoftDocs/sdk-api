---
UID: NF:wdstci.WdsTransportClientRegisterCallback
title: WdsTransportClientRegisterCallback function (wdstci.h)
description: Registers a callback with the multicast client.
helpviewer_keywords: ["WdsTransportClientRegisterCallback","WdsTransportClientRegisterCallback function [Windows Deployment Services]","wds.wdstransportclientregistercallback","wdstci/WdsTransportClientRegisterCallback"]
old-location: wds\wdstransportclientregistercallback.htm
tech.root: wds
ms.assetid: e3c809c4-5681-4979-8633-bb8d3dbde35b
ms.date: 12/05/2018
ms.keywords: WdsTransportClientRegisterCallback, WdsTransportClientRegisterCallback function [Windows Deployment Services], wds.wdstransportclientregistercallback, wdstci/WdsTransportClientRegisterCallback
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
 - WdsTransportClientRegisterCallback
 - wdstci/WdsTransportClientRegisterCallback
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
 - WdsTransportClientRegisterCallback
---

# WdsTransportClientRegisterCallback function


## -description

Registers a callback with the multicast client.

## -parameters

### -param hSessionKey [in]

Unique handle returned by the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientinitializesession">WdsTransportClientInitializeSession</a>.

### -param CallbackId [in]

Identifier specifying which callback is being registered. This parameter receives a <a href="/windows/desktop/api/wdstci/ne-wdstci-transportclient_callback_id">TRANSPORTCLIENT_CALLBACK_ID</a> enumeration value. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_SESSION_START</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientsessionstart">PFN_WdsTransportClientSessionStart</a> callback. This callback is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents">PFN_WdsTransportClientReceiveContents</a> callback. This callback is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_SESSION_COMPLETE</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete">PFN_WdsTransportClientSessionComplete</a> callback. This callback is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_RECEIVE_METADATA</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata">PFN_WdsTransportClientReceiveMetadata</a> callback. This callback is optional.

</td>
</tr>
</table>

### -param pfnCallback [in]

Pointer to the function pointer associated with this id.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

All callbacks must be registered with the client before the consumer calls <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientstartsession">WdsTransportClientStartSession</a>.  Once the session is started, no further callbacks may be registered.