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

# ITfDisplayAttributeMgr::GetDisplayAttributeInfo


## -description




## -parameters




### -param guid [in]

Contains a GUID that identifies the display attribute data requested. This value is obtained by obtaining the GUID_PROP_ATTRIBUTE property for the range of text. For more information, see <a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">ITfContext::GetProperty</a> and <a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">ITfContext::TrackProperties</a>.


### -param ppInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a> interface pointer that receives the object.


### -param pclsidOwner [out]

Pointer to a CLSID value that receives the CLSID of the display attribute provider. This parameter can be <b>NULL</b> if the CLSID is not required.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">ITfContext::GetProperty
      </a>



<a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">
        ITfContext::TrackProperties
      </a>



<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">
        ITfDisplayAttributeInfo
      </a>



<a href="https://msdn.microsoft.com/4a1f9a13-54a1-4294-9635-80eef8bcd8d5">ITfDisplayAttributeMgr</a>
 

 

