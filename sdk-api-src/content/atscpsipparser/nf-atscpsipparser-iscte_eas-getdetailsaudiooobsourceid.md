---
UID: NF:atscpsipparser.ISCTE_EAS.GetDetailsAudioOOBSourceID
title: ISCTE_EAS::GetDetailsAudioOOBSourceID
author: windows-sdk-content
description: The GetDetailsAudioOOBSourceID method returns the source identifier of the virtual audio channel for the emergency alert.
old-location: mstv\iscte_eas_getdetailsaudiooobsourceid.htm
old-project: mstv
ms.assetid: ab054225-e8e6-4f78-9010-15fc8e5ad15b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDetailsAudioOOBSourceID, GetDetailsAudioOOBSourceID method [Microsoft TV Technologies], GetDetailsAudioOOBSourceID method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetDetailsAudioOOBSourceID method, ISCTE_EAS.GetDetailsAudioOOBSourceID, ISCTE_EAS::GetDetailsAudioOOBSourceID, ISCTE_EASGetDetailsAudioOOBSourceID, atscpsipparser/ISCTE_EAS::GetDetailsAudioOOBSourceID, mstv.iscte_eas_getdetailsaudiooobsourceid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	ISCTE_EAS.GetDetailsAudioOOBSourceID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
The <a href="https://msdn.microsoft.com/f40e89f4-6a33-44a9-933c-bf38978f1cb2">ISCTE_EAS::Initialize</a> method was not called.

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




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS Interface</a>
 

 

