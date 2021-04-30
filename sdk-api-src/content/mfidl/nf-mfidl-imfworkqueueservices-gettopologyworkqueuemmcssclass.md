---
UID: NF:mfidl.IMFWorkQueueServices.GetTopologyWorkQueueMMCSSClass
title: IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass (mfidl.h)
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) class for a specified branch of the current topology.
helpviewer_keywords: ["GetTopologyWorkQueueMMCSSClass","GetTopologyWorkQueueMMCSSClass method [Media Foundation]","GetTopologyWorkQueueMMCSSClass method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","GetTopologyWorkQueueMMCSSClass method","IMFWorkQueueServices.GetTopologyWorkQueueMMCSSClass","IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass","e815bde7-e17e-4616-8a3f-688f357e8009","mf.imfworkqueueservices_gettopologyworkqueuemmcssclass","mfidl/IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass"]
old-location: mf\imfworkqueueservices_gettopologyworkqueuemmcssclass.htm
tech.root: mf
ms.assetid: e815bde7-e17e-4616-8a3f-688f357e8009
ms.date: 12/05/2018
ms.keywords: GetTopologyWorkQueueMMCSSClass, GetTopologyWorkQueueMMCSSClass method [Media Foundation], GetTopologyWorkQueueMMCSSClass method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],GetTopologyWorkQueueMMCSSClass method, IMFWorkQueueServices.GetTopologyWorkQueueMMCSSClass, IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass, e815bde7-e17e-4616-8a3f-688f357e8009, mf.imfworkqueueservices_gettopologyworkqueuemmcssclass, mfidl/IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass
 - mfidl/IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass
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
 - IMFWorkQueueServices.GetTopologyWorkQueueMMCSSClass
---

# IMFWorkQueueServices::GetTopologyWorkQueueMMCSSClass


## -description

Retrieves the Multimedia Class Scheduler Service (MMCSS) class for a specified branch of the current topology.

## -parameters

### -param dwTopologyWorkQueueId [in]

Identifies the work queue assigned to this topology branch. The application defines this value by setting the <a href="/windows/desktop/medfound/mf-toponode-workqueue-id-attribute">MF_TOPONODE_WORKQUEUE_ID</a> attribute on the source node for the branch.

### -param pwszClass [out]

Pointer to a buffer that receives the name of the MMCSS class. This parameter can be <b>NULL</b>.

### -param pcchClass [in, out]

On input, specifies the size of the <i>pwszClass</i> buffer, in characters. On output, receives the required size of the buffer, in characters. The size includes the terminating null character.

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
There is no work queue with the specified identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszClass</i> buffer is too small to receive the class name.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>