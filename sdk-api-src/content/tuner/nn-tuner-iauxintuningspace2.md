---
UID: NN:tuner.IAuxInTuningSpace2
title: IAuxInTuningSpace2
author: windows-sdk-content
description: This topic applies to Windows XP Media Center Edition 2004 and later.
old-location: mstv\iauxintuningspace2.htm
tech.root: mstv
ms.assetid: 51d92eab-1cf0-451c-aefb-ca36360e29f7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAuxInTuningSpace2, IAuxInTuningSpace2 interface [Microsoft TV Technologies], IAuxInTuningSpace2 interface [Microsoft TV Technologies],described, IAuxInTuningSpace2Interface, mstv.iauxintuningspace2, tuner/IAuxInTuningSpace2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IAuxInTuningSpace2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAuxInTuningSpace2 interface


## -description



This topic applies to Windows XP Media Center Edition 2004 and later.
        

The <b>IAuxInTuningSpace2</b> interface is implemented on <a href="https://msdn.microsoft.com/f3d0948c-aa40-4a19-a620-af75495ecde2">AuxInTuningSpace</a> objects, which represent auxiliary video inputs such as S-video or composite video on a hardware device that is connected to the computer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAuxInTuningSpace2</b> interface inherits from <a href="https://msdn.microsoft.com/fd02375b-3493-4a59-aa85-6f1528d79630">IAuxInTuningSpace</a>. <b>IAuxInTuningSpace2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAuxInTuningSpace2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dffd3ad2-2caa-4041-9e24-024050414a87">get_CountryCode</a>
</td>
<td align="left" width="63%">
Gets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c589a79-c71f-40fc-8bf2-5163ae652d70">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAuxInTuningSpace2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/fd02375b-3493-4a59-aa85-6f1528d79630">IAuxInTuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

