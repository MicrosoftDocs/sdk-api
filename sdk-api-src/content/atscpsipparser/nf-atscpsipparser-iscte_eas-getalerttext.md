---
UID: NF:atscpsipparser.ISCTE_EAS.GetAlertText
title: ISCTE_EAS::GetAlertText
author: windows-sdk-content
description: The GetAlertText method gets the alert text for a specified ISO 639 language code.
old-location: mstv\iscte_eas_getalerttext.htm
tech.root: mstv
ms.assetid: 4bef1a14-b0f6-40a0-bac0-1d6c00c120e5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetAlertText, GetAlertText method [Microsoft TV Technologies], GetAlertText method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetAlertText method, ISCTE_EAS.GetAlertText, ISCTE_EAS::GetAlertText, ISCTE_EASGetAlertText, atscpsipparser/ISCTE_EAS::GetAlertText, mstv.iscte_eas_getalerttext
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISCTE_EAS.GetAlertText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- atscpsipparser.h
: 
- ISCTE_EAS.GetAlertText
: 
---

# ISCTE_EAS::GetAlertText


## -description


The <b>GetAlertText</b> method gets the alert text for a specified ISO 639 language code.


## -parameters




### -param bstrIS0639code [in]

The ISO 639 language code.


### -param pbstrString [out]

Receives the alert text as a <b>BSTR</b>. The caller must free the string by calling <b>SysFreeString</b>.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The specified language is not present.

</td>
</tr>
</table>
 




## -remarks



The returned string is taken from the alert_text field, as defined by ANSI-J-STD-042-A.

<div class="alert"><b>Note</b>  An earlier version of the documentation gave an incorrect signature for this method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS Interface</a>
 

 

