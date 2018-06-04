---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITfFnConfigureRegisterEudc::Show


## -description


The ITfFnConfigureRegisterEudc::Show method shows the EUDC key sequence register UI.


## -parameters




### -param hwndParent [in]

[in] Handle of the parent window. The text service typically uses this as the parent or owner window when creating a dialog box.


### -param langid [in]

[in] Contains a LANGID value that specifies the identifier of the language.


### -param rguidProfile [in]

[in] Contains a GUID value that specifies the language profile identifier that the text service is under.


### -param bstrRegistered

[in, unique] Contains a BSTR that contains the EUDC to be registered with the text service. This is optional and can be <b>NULL</b>. If <b>NULL</b>, the text service should display a default register EUDC dialog box.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 



