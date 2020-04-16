---
UID: NF:wmcontainer.IMFASFStreamSelector.SetOutputOverride
title: IMFASFStreamSelector::SetOutputOverride (wmcontainer.h)
description: Sets the selection status of an output, overriding other selection criteria.helpviewer_keywords: ["IMFASFStreamSelector interface [Media Foundation]","SetOutputOverride method","IMFASFStreamSelector.SetOutputOverride","IMFASFStreamSelector::SetOutputOverride","SetOutputOverride","SetOutputOverride method [Media Foundation]","SetOutputOverride method [Media Foundation]","IMFASFStreamSelector interface","c8affecd-107f-4701-88df-200db06ad49e","mf.imfasfstreamselector_setoutputoverride","wmcontainer/IMFASFStreamSelector::SetOutputOverride"]
old-location: mf\imfasfstreamselector_setoutputoverride.htm
tech.root: medfound
ms.assetid: c8affecd-107f-4701-88df-200db06ad49e
ms.date: 12/05/2018
ms.keywords: IMFASFStreamSelector interface [Media Foundation],SetOutputOverride method, IMFASFStreamSelector.SetOutputOverride, IMFASFStreamSelector::SetOutputOverride, SetOutputOverride, SetOutputOverride method [Media Foundation], SetOutputOverride method [Media Foundation],IMFASFStreamSelector interface, c8affecd-107f-4701-88df-200db06ad49e, mf.imfasfstreamselector_setoutputoverride, wmcontainer/IMFASFStreamSelector::SetOutputOverride
f1_keywords:
- wmcontainer/IMFASFStreamSelector.SetOutputOverride
dev_langs:
- c++
req.header: wmcontainer.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFASFStreamSelector.SetOutputOverride
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFStreamSelector::SetOutputOverride


## -description



Sets the selection status of an output, overriding other selection criteria.




## -parameters




### -param dwOutputNum [in]

Output number for which to set selection.


### -param Selection [in]

Member of the <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/ne-wmcontainer-asf_selection_status">ASF_SELECTION_STATUS</a> enumeration specifying the level of selection for the output.


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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>
 

 

