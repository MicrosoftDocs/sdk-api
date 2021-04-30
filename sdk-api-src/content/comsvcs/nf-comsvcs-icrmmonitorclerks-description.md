---
UID: NF:comsvcs.ICrmMonitorClerks.Description
title: ICrmMonitorClerks::Description (comsvcs.h)
description: Retrieves the description of the CRM Compensator for the specified index.
helpviewer_keywords: ["Description","Description method [COM+]","Description method [COM+]","ICrmMonitorClerks interface","ICrmMonitorClerks interface [COM+]","Description method","ICrmMonitorClerks.Description","ICrmMonitorClerks::Description","_dtc_ICrmMonitorClerks_Description","comsvcs/ICrmMonitorClerks::Description","cos.icrmmonitorclerks_description"]
old-location: cos\icrmmonitorclerks_description.htm
tech.root: cos
ms.assetid: 3603d898-1601-419b-b3f8-3ad49f2070a0
ms.date: 12/05/2018
ms.keywords: Description, Description method [COM+], Description method [COM+],ICrmMonitorClerks interface, ICrmMonitorClerks interface [COM+],Description method, ICrmMonitorClerks.Description, ICrmMonitorClerks::Description, _dtc_ICrmMonitorClerks_Description, comsvcs/ICrmMonitorClerks::Description, cos.icrmmonitorclerks_description
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ICrmMonitorClerks::Description
 - comsvcs/ICrmMonitorClerks::Description
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitorClerks.Description
---

# ICrmMonitorClerks::Description


## -description

Retrieves the description of the CRM Compensator for the specified index.

## -parameters

### -param Index [in]

The index of the required CRM clerk as a numeric <b>Variant</b>, or the instance CLSID as a <b>Variant</b> string.

### -param pItem [out]

The description string originally provided by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-registercompensator">ICrmLogControl::RegisterCompensator</a>.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is incorrect.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorclerks">ICrmMonitorClerks</a>