---
UID: NF:devicetopology.IConnector.Disconnect
title: IConnector::Disconnect (devicetopology.h)
description: The Disconnect method disconnects this connector from another connector.
helpviewer_keywords: ["Disconnect","Disconnect method [Core Audio]","Disconnect method [Core Audio]","IConnector interface","IConnector interface [Core Audio]","Disconnect method","IConnector.Disconnect","IConnector::Disconnect","IConnectorDisconnect","coreaudio.iconnector_disconnect","devicetopology/IConnector::Disconnect"]
old-location: coreaudio\iconnector_disconnect.htm
tech.root: CoreAudio
ms.assetid: f1ca8863-4756-4d08-97b3-959a76d6f991
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [Core Audio], Disconnect method [Core Audio],IConnector interface, IConnector interface [Core Audio],Disconnect method, IConnector.Disconnect, IConnector::Disconnect, IConnectorDisconnect, coreaudio.iconnector_disconnect, devicetopology/IConnector::Disconnect
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConnector::Disconnect
 - devicetopology/IConnector::Disconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IConnector.Disconnect
---

# IConnector::Disconnect


## -description

The <b>Disconnect</b> method disconnects this connector from another connector.



## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
This connector is already disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_READ_ONLY)</b></dt>
</dl>
</td>
<td width="60%">
A permanent connection cannot be disconnected. For information about this macro, see the Windows SDK documentation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>
