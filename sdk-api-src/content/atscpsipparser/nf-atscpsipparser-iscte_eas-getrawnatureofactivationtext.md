---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawNatureOfActivationText
title: ISCTE_EAS::GetRawNatureOfActivationText (atscpsipparser.h)
author: windows-sdk-content
description: Gets the raw nature_of_activation_text field from the EAS table.
old-location: mstv\iscte_eas_getrawnatureofactivationtext.htm
tech.root: mstv
ms.assetid: 11ada9ab-b55f-41c1-9d7d-1c856a17a3a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRawNatureOfActivationText, GetRawNatureOfActivationText method [Microsoft TV Technologies], GetRawNatureOfActivationText method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawNatureOfActivationText method, ISCTE_EAS.GetRawNatureOfActivationText, ISCTE_EAS::GetRawNatureOfActivationText, atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationText, mstv.iscte_eas_getrawnatureofactivationtext
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
 - ISCTE_EAS.GetRawNatureOfActivationText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCTE_EAS::GetRawNatureOfActivationText


## -description


Gets the raw nature_of_activation_text field from the EAS table.


## -parameters




### -param pbVal [out]

A pointer to a buffer that receives the nature_of_activation_text field. The caller must allocate the buffer. To get the required size of the buffer, call <a href="https://msdn.microsoft.com/a7f93884-d8a9-449b-afc2-b2ccbd0d2492">ISCTE_EAS::GetRawNatureOfActivationTextLen</a>. The text is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the text for a specific language, call <a href="https://msdn.microsoft.com/36cb57f1-b894-4c41-b555-db15f8dbe516">ISCTE_EAS::GetNatureOfActivationText</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS</a>



<a href="https://msdn.microsoft.com/36cb57f1-b894-4c41-b555-db15f8dbe516">ISCTE_EAS::GetNatureOfActivationText</a>
 

 

