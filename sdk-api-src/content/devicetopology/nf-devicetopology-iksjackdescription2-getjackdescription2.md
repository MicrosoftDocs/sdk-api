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

# IKsJackDescription2::GetJackDescription2


## -description


The <b>GetJackDescription2</b> method gets the description of a specified audio jack.


## -parameters




### -param nJack [in]

The index of the jack to get a description for. If the connection consists of <i>n</i> jacks, the jacks are numbered from 0 to <i>n</i>– 1. To get the number of jacks, call the <a href="https://msdn.microsoft.com/b7ebe746-4680-4921-a1fd-1940e306f4eb">IKsJackDescription::GetJackCount</a> method.


### -param pDescription2 [out]

Pointer to a caller-allocated buffer into which the method writes a structure of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff537138">KSJACK_DESCRIPTION2</a> that contains information about the jack. The buffer size must be at least <code>sizeof(KSJACK_DESCRIPTION2)</code>.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nJack</i> is not a valid jack index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pDescription</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9a3d7631-6892-457a-91ab-484ae867fd9f">IKsJackDescription2</a>
 

 

