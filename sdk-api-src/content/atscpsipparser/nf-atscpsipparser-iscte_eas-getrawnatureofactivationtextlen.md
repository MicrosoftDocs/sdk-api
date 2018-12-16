---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawNatureOfActivationTextLen
title: ISCTE_EAS::GetRawNatureOfActivationTextLen
author: windows-sdk-content
description: Gets the length of the nature_of_activation_text field.
old-location: mstv\iscte_eas_getrawnatureofactivationtextlen.htm
tech.root: mstv
ms.assetid: a7f93884-d8a9-449b-afc2-b2ccbd0d2492
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRawNatureOfActivationTextLen, GetRawNatureOfActivationTextLen method [Microsoft TV Technologies], GetRawNatureOfActivationTextLen method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawNatureOfActivationTextLen method, ISCTE_EAS.GetRawNatureOfActivationTextLen, ISCTE_EAS::GetRawNatureOfActivationTextLen, atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationTextLen, mstv.iscte_eas_getrawnatureofactivationtextlen
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
 - ISCTE_EAS.GetRawNatureOfActivationTextLen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCTE_EAS::GetRawNatureOfActivationTextLen


## -description


Gets the length of the nature_of_activation_text field.


## -parameters




### -param pbVal [out]

Receives the size of the nature_of_activation_text field, in bytes. To get the value of the field, allocate a buffer of this size and call <a href="https://msdn.microsoft.com/11ada9ab-b55f-41c1-9d7d-1c856a17a3a9">ISCTE_EAS::GetRawNatureOfActivationText</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS</a>



<a href="https://msdn.microsoft.com/36cb57f1-b894-4c41-b555-db15f8dbe516">ISCTE_EAS::GetNatureOfActivationText</a>
 

 

