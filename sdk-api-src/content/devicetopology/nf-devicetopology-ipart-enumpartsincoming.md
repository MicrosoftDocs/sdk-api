---
UID: NF:devicetopology.IPart.EnumPartsIncoming
title: IPart::EnumPartsIncoming
author: windows-sdk-content
description: The EnumPartsIncoming method gets a list of all the incoming parts&#8212;that is, the parts that reside on data paths that are upstream from this part.
old-location: coreaudio\ipart_enumpartsincoming.htm
tech.root: CoreAudio
ms.assetid: 0d74837e-12d1-4d94-941e-6a81aeac1151
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: EnumPartsIncoming, EnumPartsIncoming method [Core Audio], EnumPartsIncoming method [Core Audio],IPart interface, IPart interface [Core Audio],EnumPartsIncoming method, IPart.EnumPartsIncoming, IPart::EnumPartsIncoming, IPartEnumPartsIncoming, coreaudio.ipart_enumpartsincoming, devicetopology/IPart::EnumPartsIncoming
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: devicetopology.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPart.EnumPartsIncoming
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- devicetopology.h
: 
- IPart.EnumPartsIncoming
: 
---

# IPart::EnumPartsIncoming


## -description



The <b>EnumPartsIncoming</b> method gets a list of all the incoming parts—that is, the parts that reside on data paths that are upstream from this part.




## -parameters




### -param ppParts [out]

Pointer to a pointer variable into which the method writes the address of an <a href="https://msdn.microsoft.com/3ac48781-90c2-4b23-aa68-3453091bde61">IPartsList</a> interface that encapsulates the list of parts that are immediately upstream from this part. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>EnumPartsIncoming</b> call fails,  <i>*ppParts</i> is <b>NULL</b>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppParts</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
This part has no links to upstream parts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



A client application can traverse a device topology against the direction of audio data flow by iteratively calling this method at each step in the traversal to get the list of parts that lie immediately upstream from the current part.

If this part has no links to upstream parts, the method returns error code E_NOTFOUND and does not create a parts list (<i>*ppParts</i> is <b>NULL</b>). For example, the method returns this error code if the <b>IPart</b> interface represents a connector through which data enters a device topology.




## -see-also




<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/3ac48781-90c2-4b23-aa68-3453091bde61">IPartsList Interface</a>
 

 

