---
UID: NF:tuner.IATSCComponentType.get_Flags
title: IATSCComponentType::get_Flags
author: windows-sdk-content
description: The get_Flags method queries whether an audio component is in AC-3 format.
old-location: mstv\iatsccomponenttype_get_flags.htm
old-project: mstv
ms.assetid: f89f59fd-31bf-48d6-9cb3-92504ba095a9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IATSCComponentType interface [Microsoft TV Technologies],get_Flags method, IATSCComponentType.get_Flags, IATSCComponentType::get_Flags, IATSCComponentTypeget_Flags, get_Flags, get_Flags method [Microsoft TV Technologies], get_Flags method [Microsoft TV Technologies],IATSCComponentType interface, mstv.iatsccomponenttype_get_flags, tuner/IATSCComponentType::get_Flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IATSCComponentType.get_Flags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCComponentType::get_Flags


## -description



The <b>get_Flags</b> method queries whether an audio component is in AC-3 format.




## -parameters




### -param Flags






#### - pFlags [out]

Receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>The component does not contain AC-3 audio</td>
</tr>
<tr>
<td>ATSCCT_AC3</td>
<td>The component contains AC-3 audio</td>
</tr>
</table>
 

See <a href="https://msdn.microsoft.com/fd4db1f7-7c32-4fcc-b95a-269a550311ef">ATSCComponentTypeFlags Enumeration</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/c7e05f63-b2cf-4a99-8e0f-bc7ec00463cf">IATSCComponentType Interface</a>
 

 

