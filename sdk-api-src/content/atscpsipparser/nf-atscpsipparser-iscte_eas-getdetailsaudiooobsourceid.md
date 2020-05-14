---
UID: NF:atscpsipparser.ISCTE_EAS.GetDetailsAudioOOBSourceID
title: ISCTE_EAS::GetDetailsAudioOOBSourceID (atscpsipparser.h)
description: The GetDetailsAudioOOBSourceID method returns the source identifier of the virtual audio channel for the emergency alert.helpviewer_keywords: ["GetDetailsAudioOOBSourceID","GetDetailsAudioOOBSourceID method [Microsoft TV Technologies]","GetDetailsAudioOOBSourceID method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetDetailsAudioOOBSourceID method","ISCTE_EAS.GetDetailsAudioOOBSourceID","ISCTE_EAS::GetDetailsAudioOOBSourceID","ISCTE_EASGetDetailsAudioOOBSourceID","atscpsipparser/ISCTE_EAS::GetDetailsAudioOOBSourceID","mstv.iscte_eas_getdetailsaudiooobsourceid"]
old-location: mstv\iscte_eas_getdetailsaudiooobsourceid.htm
tech.root: mstv
ms.assetid: ab054225-e8e6-4f78-9010-15fc8e5ad15b
ms.date: 12/05/2018
ms.keywords: GetDetailsAudioOOBSourceID, GetDetailsAudioOOBSourceID method [Microsoft TV Technologies], GetDetailsAudioOOBSourceID method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetDetailsAudioOOBSourceID method, ISCTE_EAS.GetDetailsAudioOOBSourceID, ISCTE_EAS::GetDetailsAudioOOBSourceID, ISCTE_EASGetDetailsAudioOOBSourceID, atscpsipparser/ISCTE_EAS::GetDetailsAudioOOBSourceID, mstv.iscte_eas_getdetailsaudiooobsourceid
f1_keywords:
- atscpsipparser/ISCTE_EAS.GetDetailsAudioOOBSourceID
dev_langs:
- c++
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- atscpsipparser.h
api_name:
- ISCTE_EAS.GetDetailsAudioOOBSourceID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCTE_EAS::GetDetailsAudioOOBSourceID


## -description


The <b>GetDetailsAudioOOBSourceID</b> method returns the source identifier of the virtual audio channel for the emergency alert.


## -parameters




### -param pwVal [out]

Receives the audio_OOB_source_ID field.
          


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
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-initialize">ISCTE_EAS::Initialize</a> method was not called.

</td>
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>
 

 

