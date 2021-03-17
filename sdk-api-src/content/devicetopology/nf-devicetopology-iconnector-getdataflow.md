---
UID: NF:devicetopology.IConnector.GetDataFlow
title: IConnector::GetDataFlow (devicetopology.h)
description: The GetDataFlow method gets the direction of data flow through this connector.
helpviewer_keywords: ["GetDataFlow","GetDataFlow method [Core Audio]","GetDataFlow method [Core Audio]","IConnector interface","IConnector interface [Core Audio]","GetDataFlow method","IConnector.GetDataFlow","IConnector::GetDataFlow","IConnectorGetDataFlow","coreaudio.iconnector_getdataflow","devicetopology/IConnector::GetDataFlow"]
old-location: coreaudio\iconnector_getdataflow.htm
tech.root: CoreAudio
ms.assetid: 55078775-2921-45c2-af27-c8ad53688293
ms.date: 12/05/2018
ms.keywords: GetDataFlow, GetDataFlow method [Core Audio], GetDataFlow method [Core Audio],IConnector interface, IConnector interface [Core Audio],GetDataFlow method, IConnector.GetDataFlow, IConnector::GetDataFlow, IConnectorGetDataFlow, coreaudio.iconnector_getdataflow, devicetopology/IConnector::GetDataFlow
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
 - IConnector::GetDataFlow
 - devicetopology/IConnector::GetDataFlow
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
 - IConnector.GetDataFlow
---

# IConnector::GetDataFlow


## -description

The <b>GetDataFlow</b> method gets the direction of data flow through this connector.

## -parameters

### -param pFlow [out]

Pointer to a variable into which the method writes the data-flow direction. The direction is one of the following <a href="/windows/win32/api/devicetopology/ne-devicetopology-dataflow">DataFlow</a> enumeration values:

In

Out

If data flows into the device through the connector, the data-flow direction is In. Otherwise, the data-flow direction is Out.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pFlow</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For a code example that calls this method, see the implementation of the SelectCaptureDevice function in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>