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

# IWMReaderAdvanced4::GetLanguage


## -description



The <b>GetLanguage</b> method retrieves information about a language supported by an output. You must specify an output number and a language index, and this method will supply the RFC1766-compliant language string.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number for which you want to identify the language.


### -param wLanguage [in]

<b>WORD</b> containing the language index of the supported language for which you want the details.


### -param pwszLanguageString [out]

Pointer to a wide-character <b>null</b>-terminated string containing the RFC1766-compliant language string. Pass <b>NULL</b> to retrieve the size of the string, which will be returned in <i>pcbLanguageStringLength</i>.


### -param pcchLanguageStringLength [in, out]

Pointer to a <b>WORD</b> containing the size of <i>pwszLanguageString</i> in wide characters. This size includes the terminating <b>null</b> character.


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
 




## -remarks



When setting the language to use for an output, you must set the value of the <b>g_wszLanguage</b> setting to the language index passed to this method as <i>wLanguage</i>. Do not use the language index assigned by the language list, which will be different.




## -see-also




<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/c63084cb-f4cf-413b-a3f1-eb6b1400ac93">IWMReaderAdvanced4::GetLanguageCount</a>
 

 

