---
UID: NS:eaptypes._EAP_INTERACTIVE_UI_DATA
title: "_EAP_INTERACTIVE_UI_DATA"
author: windows-driver-content
description: Contains configuration information for interactive UI components raised on an EAP supplicant.
old-location: eaphost\eap_interactive_ui_data.htm
old-project: EAPHost
ms.assetid: 68141611-4a1c-409e-8ed2-3d21a76640c3
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EAP_INTERACTIVE_UI_DATA, EAP_INTERACTIVE_UI_DATA structure [EAPHost], EAP_INTERACTIVE_UI_DATA_VERSION, _EAP_INTERACTIVE_UI_DATA, eaphost.eap_interactive_ui_data, eaptypes/EAP_INTERACTIVE_UI_DATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eaptypes.h
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
req.typenames: EAP_INTERACTIVE_UI_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	eaptypes.h
api_name:
-	EAP_INTERACTIVE_UI_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EAP_INTERACTIVE_UI_DATA structure


## -description


The <b>EAP_INTERACTIVE_UI_DATA</b> structure contains configuration information for interactive UI components raised on an EAP supplicant.


## -struct-fields




### -field dwVersion

The version of this data structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAP_INTERACTIVE_UI_DATA_VERSION"></a><a id="eap_interactive_ui_data_version"></a><dl>
<dt><b>EAP_INTERACTIVE_UI_DATA_VERSION</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The version of the EAP interactive UI data.

</td>
</tr>
</table>
 


### -field dwSize

The size of this entire structure, in bytes.


### -field dwDataType

An <a href="https://msdn.microsoft.com/0b3cd58c-9396-4c79-842b-76bf03aa7d7a">EAP_INTERACTIVE_UI_DATA_TYPE</a> value that specifies the type of data pointed to by <i>pbUiData</i>.


### -field cbUiData

The size of the data pointed to by <i>pbUiData</i>, in bytes.


### -field pbUiData

A pointer to an <a href="https://msdn.microsoft.com/e4b49cbd-b50d-474c-b6b5-8ff858eca424">EAP_UI_DATA_FORMAT</a> union that contains information about specific user interface components that correspond to the type specified in <i>dwDataType</i>.


## -see-also




<a href="https://msdn.microsoft.com/77595f36-140d-4d8e-af8e-63e9de0031c4">EAPHost Supplicant Structures</a>



<a href="https://msdn.microsoft.com/baa2a580-0bfc-450a-9a96-f32d00127fa4">EAP_CRED_EXPIRY_REQ</a>



<a href="https://msdn.microsoft.com/59b7f7d0-58af-4368-b3ea-6f180422a673">EAP_CRED_EXPIRY_RESP</a>



<a href="https://msdn.microsoft.com/537a90fc-4dd2-44d4-93da-949f31130ac4">EAP_CRED_REQ</a>



<a href="https://msdn.microsoft.com/714c75d8-71c7-4c3f-802a-a5e4f6ca65c2">EAP_CRED_RESP</a>



<a href="https://msdn.microsoft.com/e4b49cbd-b50d-474c-b6b5-8ff858eca424">EAP_UI DATA_FORMAT</a>



<a href="https://msdn.microsoft.com/c52ffeb8-ecee-4398-a7df-388b523c737c">SSO Password Change Behavior</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

